private Mono<List<ResponseResult>> executeSynQuires(List<Query> queryList, String ProdParallelFlag) throws ExecutionException, InterruptedException {
        List<ResponseResult> synResponse = new ArrayList<>();
        Iterator iterator = queryList.listIterator();
        while (iterator.hasNext()) {
            Query query = (Query) iterator.next();
            if (query.getMode() != null && query.getMode().equals(DataSyncConstant.SYNC)) {
                ToolsRequestQuery toolsRequestQuery = new ToolsRequestQuery();
                toolsRequestQuery.setApiName(DataSyncConstant.DATA_SYNC_API_NAME);
                toolsRequestQuery.setQuery(query.getQueryId());
                if (!ProdParallelFlag.equalsIgnoreCase("Y")) {
                    if (ProdParallelFlag.equalsIgnoreCase("N") && query != null && query.getSchemaName() != null) {
                        toolsRequestQuery.setDbName(query.getSchemaName());
                    } else {
                        toolsRequestQuery.setDbName(DataCompareConstants.PRIMARY_DB_SCHEMA);
                    }
                }
                Map<String, Object> param = new LinkedHashMap<>(query.getValues());
                if (query.getWhere() != null)
                    param.putAll(query.getWhere());
                toolsRequestQuery.setParams(param.values().toArray());
                synResponse.add(queryService.executeQuery(toolsRequestQuery).toFuture().get());
            }
        }
        return Mono.just(synResponse);
    }
	
	
	================
	private String queryId;
	private String tableName;
	private String operation;
	private String mode;
	private String schemaName;
	private Map<String, Object> values;
	private Map<String, Object> where;

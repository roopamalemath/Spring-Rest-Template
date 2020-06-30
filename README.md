# Spring-Rest-Template

Resttemplate is the one where we can used to invoke the external service which is exposed using http.
Syntax : New RestTemplate.getForEntity("uri", ResponseBean.class, MappingVariablesToURi)
ex : 


Map<String, String> uriVariables=new HashMap<>();
	uriVariables.put("from", from
ResponseEntity<CurrencyConversionBean> responseEntity=new RestTemplate().getForEntity("http://localhost:8081/currency-exchange/from/{from}/to/{to}", 
														  CurrencyConversionBean.class, 
														  uriVariables);
	// get the actual repsonse object
	CurrencyConversionBean response=responseEntity.getBody();

property naming convention should be same in both the class when mapping properties from one class to another

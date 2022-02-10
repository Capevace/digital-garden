# SPARQL
#studium #ai

- SPARQL over HTTP
- Using Apache Jena Fuseki (HTTP server with SPARQL queries)
- Endpoint `/api/update`

## Select

```sparql



```


## Examples

### Select

```sparql

PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>	
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX o: <http://www.ens-fiti.de/ontologies/user/order#> 
PREFIX c: <http://www.ens-fiti.de/ontologies/user/customer#> 


# Selecting all:
SELECT ?s ?p ?o
WHERE {
   ?s 	?p 	?o.		 
}


SELECT ?subject ?predicate ?object
WHERE {
  ?subject ?predicate ?object
  Filter(STRSTARTS(str(?subject), "http://www.ens-fiti.de/ontologies/user/order#")).
}
order by ?subject


# Selecting all order ids:
SELECT ?id
WHERE {
   ?order	o:orderid	?id.
}


# Selecting all orderids and orderyears:
SELECT ?id ?year
WHERE {
   ?order	rdf:type	o:order;
          	o:orderid	?id;
			o:orderyear	?year.
}


# Selecting all orderids, orderyears and orderdates:
SELECT ?id ?year ?date
WHERE {
   ?order	rdf:type	o:order;
          	o:orderid	?id;
			o:orderyear	?year;
			o:orderdate	?date.
}


# Selecting all orderids, orderyears and optional orderdates:
SELECT ?id ?year ?date
WHERE {
   ?order	rdf:type	o:order;
          	o:orderid	?id;
			o:orderyear	?year.
   OPTIONAL	{?order o:orderdate ?date}.
}


# Filtering orders:
SELECT ?id ?year
WHERE {
   ?order	rdf:type	o:order;
          	o:orderid	?id;
			o:orderyear	?year.
   Filter(?year = "2019"^^xsd:int).
   OPTIONAL{?order o:orderdate ?date}.
}


SELECT ?id ?year ?cid
WHERE {
  ?x rdf:type o:order.
  ?x o:orderid ?id.
  ?x o:orderyear ?year.
  ?x o:customer ?cust.
  ?cust c:customerid ?cid.
  OPTIONAL{
    ?x o:orderdate ?date.
    # Filter(?date = "2019-05-05"^^xsd:date).
  }.
  Filter(?date = "2019-05-05"^^xsd:date).
}

```

### Insert Data

```sparql

# SPARQL – DELETE

DELETE { ?s ?p ?o } WHERE { ?s ?p ?o };

PREFIX xsd: <http://www.w3.org/2001/XMLSchema#>
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>	
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX o: <http://www.ens-fiti.de/ontologies/user/order#> 
PREFIX c: <http://www.ens-fiti.de/ontologies/user/customer#> 

################
# Inserting Data
################

INSERT DATA
{
	o:1-505-2019	o:mandant			"1"^^xsd:int;
					o:orderid 			"505"^^xsd:long;
					o:orderyear 		"2019"^^xsd:int;
					o:customerid		"10005"^^xsd:string.


	o:1-606-2020	o:mandant			"1"^^xsd:int;
					o:orderid 			"606"^^xsd:long;
					o:orderyear 		"2020"^^xsd:int;
					o:customerid		"10006"^^xsd:string.
};


#################
# Adding Metadata
#################

INSERT DATA
{
   o:order			rdf:type	 		rdfs:Class.

   o:mandant		rdf:type 			rdf:Property;
					rdfs:domain			o:order;
					rdfs:range			xsd:int.

   o:orderid 		rdf:type 			rdf:Property;
					rdfs:domain			o:order;
					rdfs:range			xsd:long.

   o:orderyear 		rdf:type 			rdf:Property;
					rdfs:domain			o:order;
					rdfs:range			xsd:int.

   o:customerid 	rdf:type 			rdf:Property;
					rdfs:domain			o:order;
					rdfs:range			xsd:string.
};

#########################
# Adding metadata to data
#########################

INSERT DATA
{
	o:1-505-2019	rdf:type			o:order.


	o:1-606-2020	rdf:type			o:order.
};

##################
#Adding properties
##################

INSERT DATA
{

   o:orderdate 		rdf:type 			rdf:Property;
					rdfs:domain			o:order;
					rdfs:range			xsd:date.

   o:1-505-2019		o:orderdate			"2019-05-05"^^xsd:date.
};


INSERT DATA
{
   c:customer		rdf:type	 		rdfs:Class.

   c:customerid 	rdf:type 			rdf:Property;
					rdfs:domain			c:customer;
					rdfs:range			xsd:string.

   c:customerlastname 		rdf:type 			rdf:Property;
					rdfs:domain			c:customer;
					rdfs:range			xsd:string.
};

INSERT DATA
{
   c:10001			rdf:type			c:customer;
					c:customerid		"10001"^^xsd:string;
					c:customerlastname 		"Name1"^^xsd:string.

   c:10002			rdf:type			c:customer;
					c:customerid		"10002"^^xsd:string;
					c:customerlastname 		"Name2"^^xsd:string.
};

INSERT DATA
{

   o:customer 		rdf:type 			rdf:Property;
					rdfs:domain			o:order;
					rdfs:range			c:customer.

   o:1-505-2019		o:customer			c:10001.
   o:1-606-2020 	o:customer			c:10002.
};


```
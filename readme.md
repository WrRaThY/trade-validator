note: some of the validations were implemented using simply javax validation

<h2> not mandatory requirements </h2>
<h3> metrics </h3>
available under http://localhost:8080/metrics/priv.rdo.trade.endpoint.TradeValidationEndpoint.trades.* 

<h3>approach for providing high availability of the service and its scalability</h3>
since the service is stateless and has no database it can be scaled without any problems<br>
both high availability and scalability can be obtained by hosting this solution in a cloud (for example AWS)<br>
hosting in multiple availability zones provides high availability<br>
using an auto-scaling group provides scalability and in this case is not burdened with any synchronisation between nodes, because servers are be (as I already mentioned) 
stateless<br>
the external service for checking holidays might become unstable under heavy load, but we could use caching for that and I believe that in most cases simplistic approach with 
@Cacheable annotation might be enough<br>
in general this subject is not trivial and I have no idea how deep should I go, so I'll just stop here by saying that we can talk about that on a technical test

<h3>online documentation</h3>
available under http://localhost:8080/documentation

<h3>GUI where one could enter trade information, do the validation and display the status of it</h3>
swagger interface seems good enough for the job<br>
and seriously now - I simply didn't have time for that

<h2> assumptions </h2>
most of my assumptions were based on that: based on that:
http://www.investopedia.com/terms/o/option.asp
http://www.investopedia.com/terms/f/futures.asp
http://www.investopedia.com/terms/s/spottrade.asp
https://comparic.pl/futures-spot-swap-forward-put-call-podstawowe-definicje-zwiazane-z-zabezpieczeniem-ryzyka-walutowego/

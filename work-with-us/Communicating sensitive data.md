Researchers cannot always share the raw data of their analysis. This is in tension with interactive dataviz, which expose publicly the data.

#### Right level of abstraction

The easiest solution is perhaps to find a degree of aggregation. As a rule of thumb any category with at least 5 individuals might be enough. But it depends on the context; who is at stake by exposing the data? What is gain by sharing the data publicly?

#### API Proxy

The dataviz is making use of data through an API proxy, allowing for fine-grained authentification. With right level of authentification, some users might have access to some part (or certain level of granulaity) of the viz but not others. The full dataset is never exposed at once. 

With this approach, the aggregated datasets can be made even more private, as the aggregated data does not need to be served to the client (as with static hosting or prerendering).

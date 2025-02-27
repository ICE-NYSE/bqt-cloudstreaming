
# NYSE BQTMessage Consumer

This repository has sample code snippets for Java, Node.js and Python to test the NYSE BQT Kafka connectivity. The NYSE Best Quote and Trades (BQT) is a cost efficient, consolidated market data feed that provides a unified view of quotes and trades from NYSE, NYSE American, NYSE Arca, NYSE Chicago and NYSE National. More details [here.](https://www.nyse.com/market-data/real-time/nyse-bqt) 
 
## Prerequisites
Make sure that you follow the steps to configure the necessary connections in your AWS account to establish connectivity to the NYSE BQT Kafka offering. We have 2 environments for this offering viz. Load Test and Prod. Please see respective cloud onboarding documentation below:

| Environment                    | Documentation Link                                                                        |
|--------------------------------|-------------------------------------------------------------------------------------------|
| NYSE Kafka Cluster Load Test   | https://www.nyse.com/publicdocs/nyse/data/NYSE_Kafka_Cluster_Load_Test_Environment.pdf    |
| NYSE Kafka Cluster Production  | https://www.nyse.com/publicdocs/nyse/data/NYSE_Kafka_Cluster_Production_Environment.pdf   |

## FAQs

### What is NYSE Cloud Streaming?
NYSE Cloud Streaming is a new offering that expands accessibility of our high-quality exchange data feeds, now available via Amazon Web Services (AWS). While NYSE historical data feeds have been available on AWS Cloud for over the past three years, we are happy to announce that you can now access NYSE streaming real-time data feeds via cloud too.

### Why NYSE Cloud Streaming?
As data providers, we understand the importance of providing real-time data feeds to a wider range of cloud-native customers. Our goal is to equip more customers with market insights that allow them to make smarter decisions; that’s why we chose Redpanda® to stream our data, making it available to you at a faster rate and lower cost than traditional data feeds.

### What is the architecture behind NYSE Cloud Streaming?
![NYSE Cloud Streaming](https://github.com/ICE-NYSE/bqt-cloudstreaming/blob/main/assets/NYSE-Cloud-Streaming-architecture.png)

### What kind of data feeds are offered via this service?
Currently, NYSE offers Best Quotes and Trades aka BQT feed via this offering. BQT is a cost-efficient, consolidated market data feed that provides a unified view of quotes and trades from NYSE, NYSE American, NYSE Arca, NYSE Chicago, and NYSE National. We plan to add more data feeds in the future.

### I am in Seoul, how can I get fastest access to NYSE Cloud Streaming?
No problem. We provide seamless connectivity for cloud streaming in these regions across the world : North America (N.California, Ohio, Canada Central), Europe (Stockholm, Paris, London, Milan, Frankfurt), Africa (Cape Town), Middle East (Bahrain) and Asia Pacific (Osaka, Hong Kong, Seoul, Mumbai). We are adding more regions soon and can provide custom connectivity outside of these regions too. For more details about global access for cloud streaming please reach out to us @ <Dev-NYSE-Cloud@ice.com>.

### Where can I see the client specification documentation for BQT?
Client specs are available [here.](https://www.nyse.com/publicdocs/nyse/data/NYSE_BQT_Client_Specification.pdf) 

### What is the message format used for this offering?
We use protocol buffers as the message format. Our client specification is available here and our proto file is accessible via this link.

### Where can I find sample code snippets to connect to the NYSE Cloud Streaming offering?
This github repository has different code samples for java, nodejs and python.

### What is the typical latency expected for this offering?
Our typical latencies for consumers in the North Virginia region of AWS are about 30-50 milliseconds and 200-300 milliseconds in Hong Kong. https://www.cloudping.co/ has details about latency profiles between different AWS regions.

### How long is the data stored in the Kafka cluster?
We store the current day's worth of market data in the Kafka cluster.

### When should the connections be established by consumers for data consumption?
| Feed     | Start Time (EST) | Stop Time (EST) |
|----------|------------------|-----------------|
| NYSE BQT | 1 AM             | 8 PM            |


For more information: <Dev-NYSE-Cloud@ice.com>

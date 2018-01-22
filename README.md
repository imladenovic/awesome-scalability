# Awesome Scalability, Availability, and Stability Back-end Design Patterns
[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of selected readings to illustrate Scalability, Availability, and Stability Design Patterns in Back-end Development.

#### What if your backend went slow?
> Understand your problems: performance problem (slow for a single user) or scalability problem (fast for a single user but slow under heavy load) by reviewing [design principles as well as best pratices](#principles).

#### What if your backend went down?
> "Even if you lose all one day, you can build all over again if you retain your calm!" - Thuan Pham, CTO at Uber Technologies Inc.

## Contributing

Please take a look at the [contribution guidelines](CONTRIBUTING.md) first.
Contributions are always welcome!

## Contents
- [Principles](#principles)
- [Scalability](#scalability)
- [Availability](#availability)
- [Stability](#stability)
- [Other Design Aspects](#others)
- [Books](#books)
- [Talks](#talks)

## Principles
* [CAP Theorem and Trade-offs](http://robertgreiner.com/2014/08/cap-theorem-revisited/)	
* [Scaling Up and Scaling Out](https://blogs.technet.microsoft.com/admoore/2015/02/17/scaling-out-vs-scaling-up/)
* [ACID and BASE](https://neo4j.com/blog/acid-vs-base-consistency-models-explained/)
* [Blocking/Non-Blocking and Sync/Async](https://blogs.msdn.microsoft.com/csliu/2009/08/27/io-concept-blockingnon-blocking-vs-syncasync/)
* [Why Non-Blocking?](https://techblog.bozho.net/why-non-blocking/)
* [SQL and NoSQL](https://www.upwork.com/hiring/data/sql-vs-nosql-databases-whats-the-difference/)
* [Consistent Hashing - Explained by Tom White, author of 'Hadoop: the Definitive Guide'](http://www.tom-e-white.com/2007/11/consistent-hashing.html)
* [Cache is King!](https://www.stevesouders.com/blog/2012/10/11/cache-is-king/)
* [Understand Latency](http://highscalability.com/latency-everywhere-and-it-costs-you-sales-how-crush-it)
* [Architecture Issues When Scaling Web Applications: Bottlenecks, Database, CPU, IO](http://highscalability.com/blog/2014/5/12/4-architecture-issues-when-scaling-web-applications-bottlene.html)	
* [20 Common Bottlenecks](http://highscalability.com/blog/2012/5/16/big-list-of-20-common-bottlenecks.html)
* [Relying on Software to Redirect Traffic Reliably at Various Layers](https://www.usenix.org/conference/srecon15/program/presentation/taveira)
* [Advantages and Drawbacks of Microservices](https://cloudacademy.com/blog/microservices-architecture-challenge-advantage-drawback/)
* [Breaking Things on Purpose](https://www.usenix.org/conference/srecon17americas/program/presentation/andrus)
* [Avoid Overengineering](https://medium.com/@rdsubhas/10-modern-software-engineering-mistakes-bc67fbef4fc8)
* [Design for Loose-coupling](https://dzone.com/articles/the-importance-of-loose-coupling-in-rest-api-desig)
* [Design for Resiliency](http://highscalability.com/blog/2012/12/31/designing-for-resiliency-will-be-so-2013.html)
* [Design for Self-healing when failures occur](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/self-healing)
* [Design for Scale out](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/scale-out)
* [Best Practices for Scaling Out](https://blog.openshift.com/best-practices-for-horizontal-application-scaling/)	
* [Design for Evolution](https://docs.microsoft.com/en-us/azure/architecture/guide/design-principles/design-for-evolution)	

## Scalability
* [Microservices](https://hackernoon.com/microservices-are-hard-an-invaluable-guide-to-microservices-2d06bd7bcf5d)
	* [Thinking Inside the Container - Riot Games (8 part series)](https://engineering.riotgames.com/news/thinking-inside-container)
	* [Containerization at Pinterest](https://medium.com/@Pinterest_Engineering/containerization-at-pinterest-92295347f2f3)
	* [The Evolution of Container Usage at Netflix](https://medium.com/netflix-techblog/the-evolution-of-container-usage-at-netflix-3abfc096781b)
	* [Dockerizing MySQL at Uber](https://eng.uber.com/dockerizing-mysql/)
	* [Testing of Microservices at Spotify](https://labs.spotify.com/2018/01/11/testing-of-microservices/)
* [Distributed Caching](https://www.wix.engineering/single-post/scaling-to-100m-to-cache-or-not-to-cache)
	* [Write-behind and Write-through](https://docs.oracle.com/cd/E15357_01/coh.360/e15723/cache_rtwtwbra.htm#COHDG5177)
	* [Eviction Policies](http://highscalability.com/blog/2016/1/25/design-of-a-modern-cache.html)
	* [Peer-To-Peer Caching](https://en.wikipedia.org/wiki/P2P_caching)
	* [Distributed Caching at Netflix with EVCache](https://medium.com/netflix-techblog/caching-for-a-global-netflix-7bcc457012f1)
	* [Robust Memcache Traffic Analyzer at Box.com](https://blog.box.com/blog/introducing-memsniff-robust-memcache-traffic-analyzer/)
	* [How Etsy caches: Consistent Hashing and Cache Smearing](https://codeascraft.com/2017/11/30/how-etsy-caches/)
* [Distributed Tracking and Tracing](https://www.oreilly.com/ideas/understanding-the-value-of-distributed-tracing)
	* [Tracking Service Infrastructure at Scale at Spotify](https://www.usenix.org/conference/srecon17americas/program/presentation/arthorne)
	* [Distributed Tracing with Pintrace at Pinterest](https://medium.com/@Pinterest_Engineering/distributed-tracing-at-pinterest-with-new-open-source-tools-a4f8a5562f6b)
	* [Analyzing Distributed Trace Data at Pinterest](https://medium.com/@Pinterest_Engineering/analyzing-distributed-trace-data-6aae58919949)
	* [Distributed Tracing at Uber](https://eng.uber.com/distributed-tracing/)
* [Distributed Logging](https://blog.treasuredata.com/blog/2016/08/03/distributed-logging-architecture-in-the-container-era/)	
	* [Scalable and reliable log ingestion at Pinterest](https://medium.com/@Pinterest_Engineering/scalable-and-reliable-data-ingestion-at-pinterest-b921c2ee8754)
	* [Building DistributedLog at Twitter: High-performance replicated log service](https://blog.twitter.com/engineering/en_us/topics/infrastructure/2015/building-distributedlog-twitter-s-high-performance-replicated-log-servic.html)
	* [Logging Service with Spark at CERN Accelerator](https://databricks.com/blog/2017/12/14/the-architecture-of-the-next-cern-accelerator-logging-service.html)
	* [Logging and Aggregation at Quora](https://engineering.quora.com/Logging-and-Aggregation-at-Quora)
	* [BookKeeper: Distributed Log Storage at Yahoo](https://yahooeng.tumblr.com/post/109908973316/bookkeeper-yahoos-distributed-log-storage-is)
* [Distributed Messaging](https://arxiv.org/pdf/1704.00411.pdf)
	* [Understanding When to use RabbitMQ or Apache Kafka](https://content.pivotal.io/blog/understanding-when-to-use-rabbitmq-or-apache-kafka)
	* [Running Kafka at scale at Linkedin](https://engineering.linkedin.com/kafka/running-kafka-scale)
	* [Delaying Asynchronous Message Processing with RabbitMQ at Indeed](http://engineering.indeedblog.com/blog/2017/06/delaying-messages/)
	* [Real-time Data Pipeline with Kafka at Yelp](https://engineeringblog.yelp.com/2016/07/billions-of-messages-a-day-yelps-real-time-data-pipeline.html)
	* [Audit Kafka End-to-End at Uber (count each message exactly once, audit a message across tiers)](https://eng.uber.com/chaperone/)
	* [Deduplication Techniques](https://en.wikipedia.org/wiki/Data_deduplication)
		* [Real-time Deduping at Scale with Kafka-based Pipleline at Tapjoy](http://eng.tapjoy.com/blog-list/real-time-deduping-at-scale)
		* [Delivering Billions of Messages Exactly Once: Deduping at Segment](https://segment.com/blog/exactly-once-delivery/)		
* [Storage](http://highscalability.com/blog/2011/11/1/finding-the-right-data-solution-for-your-application-in-the.html)
	* [In-memory Storage](https://medium.com/@denisanikin/what-an-in-memory-database-is-and-how-it-persists-data-efficiently-f43868cff4c1)
		* [Optimizing Memcached Efficiency at Quora](https://engineering.quora.com/Optimizing-Memcached-Efficiency)
		* [Real-Time Data Warehouse with MemSQL on Cisco UCS](https://blogs.cisco.com/datacenter/memsql)
		* [Moving to MemSQL for solving problems at Tapjoy: horizontally scalable, ACID compliant, MySQL compatibility](http://eng.tapjoy.com/blog-list/moving-to-memsql)
	* [Durable Storage (typically Object Storage)](http://www.datacenterknowledge.com/archives/2013/10/04/object-storage-the-future-of-scale-out)
		* [Amazon S3](https://aws.amazon.com/s3/)
			* [Reasons for Choosing S3 over HDFS at Databricks](https://databricks.com/blog/2017/05/31/top-5-reasons-for-choosing-s3-over-hdfs.html)
			* [S3 in the Data Infrastructure at Airbnb](https://medium.com/airbnb-engineering/data-infrastructure-at-airbnb-8adfb34f169c)
			* [Quantcast File System on Amazon S3](https://www.quantcast.com/blog/quantcast-file-system-on-amazon-s3/)
			* [Using S3 in Netflix Chukwa](https://medium.com/netflix-techblog/evolution-of-the-netflix-data-pipeline-da246ca36905)	
		* [Yahoo Cloud Object Store - Object Storage at Exabyte Scale](https://yahooeng.tumblr.com/post/116391291701/yahoo-cloud-object-store-object-storage-at)

* [NoSQL](https://www.thoughtworks.com/insights/blog/nosql-databases-overview)
	* [Key-Value Databases (DynamoDB, Voldemort, Manhattan)](http://highscalability.com/anti-rdbms-list-distributed-key-value-stores)
		* [Scaling Mapbox infrastructure with DynamoDB Streams](https://blog.mapbox.com/scaling-mapbox-infrastructure-with-dynamodb-streams-d53eabc5e972)
		* [Manhattan: Twitter’s distributed key-value database](https://blog.twitter.com/engineering/en_us/a/2014/manhattan-our-real-time-multi-tenant-distributed-database-for-twitter-scale.html)
		* [Sherpa: Yahoo’s distributed NoSQL key-value store](https://yahooeng.tumblr.com/post/120730204806/sherpa-scales-new-heights)
	* [Column Databases (Cassandra, HBase, Vertica, Sybase IQ)](https://aws.amazon.com/nosql/columnar/)
		* [Consistent Hashing in Cassandra](https://blog.imaginea.com/consistent-hashing-in-cassandra/)
		* [When NOT to use Cassandra?](https://stackoverflow.com/questions/2634955/when-not-to-use-cassandra)
		* [Storing Images in Cassandra at Walmart Scale](https://medium.com/walmartlabs/building-object-store-storing-images-in-cassandra-walmart-scale-a6b9c02af593)
		* [Cassandra at Instagram](https://www.slideshare.net/DataStax/cassandra-at-instagram-2016)
		* [How Yelp Scaled Ad Analytics with Cassandra](https://engineeringblog.yelp.com/2016/08/how-we-scaled-our-ad-analytics-with-cassandra.html)
		* [How Discord Stores Billions of Messages with Cassandra](https://blog.discordapp.com/how-discord-stores-billions-of-messages-7fa6ec7ee4c7)
	* [Document Databases (MongoDB, CouchDB)](https://msdn.microsoft.com/en-us/magazine/hh547103.aspx)
		* [eBay: Building Mission-Critical Multi-Data Center Applications with MongoDB](https://www.mongodb.com/blog/post/ebay-building-mission-critical-multi-data-center-applications-with-mongodb)
		* [MongoDB at Baidu: Multi-Tenant Cluster Storing 200+ Billion Documents across 160 Shards](https://www.mongodb.com/blog/post/mongodb-at-baidu-powering-100-apps-across-600-nodes-at-pb-scale)
		* [The AWS and MongoDB Infrastructure of Parse (acquired by Facebook)](https://medium.baqend.com/parse-is-gone-a-few-secrets-about-their-infrastructure-91b3ab2fcf71)
		* [Couchbase Ecosystem at LinkedIn](https://engineering.linkedin.com/blog/2017/12/couchbase-ecosystem-at-linkedin)
	* [Graph Databases](https://www.ibm.com/developerworks/library/cl-graph-database-1/index.html)		
		* [Neo4j case studies with Walmart, eBay, AirBnB, NASA, etc](https://neo4j.com/customers/)
		* [FlockDB: Distributed Graph Database for Storing Adjancency Lists at Twitter](https://blog.twitter.com/engineering/en_us/a/2010/introducing-flockdb.html)
		* [Amazon Neptune](https://aws.amazon.com/neptune/)
	* [Datastructure Databases (Redis, Hazelcast)](https://db-engines.com/en/system/Hazelcast%3BMemcached%3BRedis)
		* [How Twitter Uses Redis To Scale](http://highscalability.com/blog/2014/9/8/how-twitter-uses-redis-to-scale-105tb-ram-39mm-qps-10000-ins.html)
		* [How Twitter Uses Redis To Scale - Video](https://www.youtube.com/watch?v=QznaOSk20nU)
		* [Scaling Slack’s Job Queue with Redis](https://slack.engineering/scaling-slacks-job-queue-687222e9d100)
		* [Moving persistent data out of Redis at Github](https://githubengineering.com/moving-persistent-data-out-of-redis/)
	* [Practical NoSQL resilience design pattern for the enterprise (eBay)](https://www.ebayinc.com/stories/blogs/tech/practical-nosql-resilience-design-pattern-for-the-enterprise/)		
* [RDBMS (MySQL, MSSQL, PostgreSQL)](https://www.mysql.com/products/cluster/scalability.html)
	* [MS SQL versus MySQL](https://www.upwork.com/hiring/data/sql-vs-mysql-which-relational-database-is-right-for-you/)
	* [Why SQL is beating NoSQL, and what this means for the future of data](https://blog.timescale.com/why-sql-beating-nosql-what-this-means-for-future-of-data-time-series-database-348b777b847a)
	* [Sharding MySQL at Pinterest](https://medium.com/@Pinterest_Engineering/sharding-pinterest-how-we-scaled-our-mysql-fleet-3f341e96ca6f)
	* [How Airbnb Partitioned Main MySQL Database in Two Weeks](https://medium.com/airbnb-engineering/how-we-partitioned-airbnb-s-main-database-in-two-weeks-55f7e006ff21)
	* [Replication is the Key for Scalability & High Availability](http://basho.com/posts/technical/replication-is-the-key-for-scalability-high-availability/)
	* [How Twitch uses PostgreSQL](https://blog.twitch.tv/how-twitch-uses-postgresql-c34aa9e56f58)
	* [Scaling MySQL-based financial reporting system at Airbnb](https://medium.com/airbnb-engineering/tracking-the-money-scaling-financial-reporting-at-airbnb-6d742b80f040)
	* [Scaling to 100M at Wix: MySQL is a Better NoSQL](https://www.wix.engineering/single-post/scaling-to-100m-mysql-is-a-better-nosql)
	* [Why Uber Engineering Switched from Postgres to MySQL](https://eng.uber.com/mysql-migration/)
	* [Handling Growth with Postgres at Instagram](https://engineering.instagram.com/handling-growth-with-postgres-5-tips-from-instagram-d5d7e7ffdfcb)
* [Time Series Database (TSDB)](https://www.influxdata.com/time-series-database/)
	* [Beringei: high-performance time series storage engine at Facebook](https://code.facebook.com/posts/952820474848503/beringei-a-high-performance-time-series-storage-engine/)	
	* [Atlas: In-memory dimensional time series database at Netflix](https://medium.com/netflix-techblog/introducing-atlas-netflixs-primary-telemetry-platform-bd31f4d8ed9a)
	* [Heroic: in-house time series database of Spotify](https://labs.spotify.com/2015/11/17/monitoring-at-spotify-introducing-heroic/)
* [HTTP Caching (Reverse Proxy, CDN)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching)
	* [Reverse Proxy (Nginx, Varnish, Squid, rack-cache)](https://www.mertech.com/overview-reverse-proxying/)
	* [Stop worrying and love the proxy](https://blog.turbinelabs.io/how-we-learned-to-stop-worrying-and-love-the-proxy-89af98fabaf8)
	* [Playing HTTP Tricks with Nginx](https://www.elastic.co/blog/playing-http-tricks-nginx)
	* [Using CDN to improve site performance at Coursera](https://building.coursera.org/blog/2015/07/09/improving-coursera-global-site-performance-a-head-to-head-cdn-battle-with-production-traffic/)
	* [Strategy: Caching 404s Saved 66% On Server Time at The Onion](http://highscalability.com/blog/2010/3/26/strategy-caching-404s-saved-the-onion-66-on-server-time.html)
* [Concurrency](https://lambda.grofers.com/open-sourcing-codon-workflow-framework-for-building-aggregator-apis-f8e591a158b4)
	* [Message-Passing Concurrency](https://link.springer.com/chapter/10.1007/978-3-642-35170-9_11)
	* [Software Transactional Memory](https://dl.acm.org/citation.cfm?id=3037750)
	* [Dataflow Concurrency](http://www.marketwired.com/press-release/java-concurrency-and-scalability-platform-akka-celebrates-fifth-anniversary-1928674.htm)
	* [Shared-State Concurrency](https://common-lisp.net/project/ssc/darcs/spec/specification.pdf)
	* [Concurrency series by Larry Osterman (Principal SDE at Microsoft)](https://social.msdn.microsoft.com/Profile/Larry%2bOsterman%2b%5BMSFT%5D/activity)
		* [Part 8 – Concurrency for scalability](https://blogs.msdn.microsoft.com/larryosterman/2005/02/28/concurrency-part-8-concurrency-for-scalability/)
		* [Part 9 - APIs that enable scalable programming](https://blogs.msdn.microsoft.com/larryosterman/2005/03/02/concurrency-part-9-apis-that-enable-scalable-programming/)
		* [Part 10 - How do you know if you’ve got a scalability issue?](https://blogs.msdn.microsoft.com/larryosterman/2005/03/03/concurrency-part-10-how-do-you-know-if-youve-got-a-scalability-issue/)
		* [Part 11 – Hidden scalability issues](https://blogs.msdn.microsoft.com/larryosterman/2005/03/04/concurrency-part-11-hidden-scalability-issues/)
		* [Part 12 – Hidden scalability issues (cont)](https://blogs.msdn.microsoft.com/larryosterman/2005/03/07/concurrency-part-12-hidden-scalability-issues-part-2/)
* [Event-Driven Architecture](https://martinfowler.com/articles/201701-event-driven.html)
	* [Messaging](https://www.ibm.com/support/knowledgecenter/en/SSAW57_8.5.5/com.ibm.websphere.nd.doc/ae/cjt1004_.html)
		* [Publish-Subscribe](https://aws.amazon.com/pub-sub-messaging/)
			* [Autoscaling Pub-Sub Consumers at Spotify](https://labs.spotify.com/2017/11/20/autoscaling-pub-sub-consumers/)
			* [Pulsar: Pub-Sub Messaging at Scale at Yahoo](https://yahooeng.tumblr.com/post/150078336821/open-sourcing-pulsar-pub-sub-messaging-at-scale)
			* [Wormhole: Pub-Sub system at Facebook (2013)](https://code.facebook.com/posts/188966771280871/wormhole-pub-sub-system-moving-data-through-space-and-time/)
		* [Point-to-Point](https://content.pivotal.io/blog/understanding-when-to-use-rabbitmq-or-apache-kafka)
		* [Store-Forward](https://medium.com/netflix-techblog/announcing-suro-backbone-of-netflixs-data-pipeline-5c660ca917b6)
		* [Request-Reply](http://edwardost.github.io/talend/camel/2015/05/15/Scalable-JMS-Request-Reply/)
	* [Actors: Fire-forget and Fire-Receive-Eventually](https://doc.akka.io/docs/akka/2.5.5/scala/actors.html)
	* [Enterprise Service Bus](http://www.oracle.com/technetwork/articles/soa/ind-soa-esb-1967705.html)
	* [Domain Events](https://www.oreilly.com/ideas/the-evolution-of-scalable-microservices)
	* [Event Stream Processing](https://www.sas.com/en_us/insights/articles/big-data/3-things-about-event-stream-processing.html)
		* [Kafka Streams on Heroku](https://blog.heroku.com/kafka-streams-on-heroku)
		* [Bullet: Forward-Looking Query Engine for Streaming Data at Yahoo](https://yahooeng.tumblr.com/post/161855616651/open-sourcing-bullet-yahoos-forward-looking)
		* [Benchmarking Streaming Computation Engines at Yahoo](https://yahooeng.tumblr.com/post/135321837876/benchmarking-streaming-computation-engines-at)
	* [Event Sourcing](https://medium.com/lcom-techblog/scalable-microservices-with-event-sourcing-and-redis-6aa245574db0)
	* [Command & Query Responsibility Segregation (CQRS)](https://docs.microsoft.com/en-us/azure/architecture/patterns/cqrs)
* [Load Balancing](https://blog.vivekpanyam.com/scaling-a-web-service-load-balancing/)
	* [Introduction to Modern Network Load Balancing and Proxying](https://blog.envoyproxy.io/introduction-to-modern-network-load-balancing-and-proxying-a57f6ff80236)
	* [Load Balancing infrastructure to support more than 1.3 billion users at Facebook](https://www.usenix.org/conference/srecon15europe/program/presentation/shuff)
	* [Load Balancing with Eureka at Netflix](https://medium.com/netflix-techblog/netflix-shares-cloud-load-balancing-and-failover-tool-eureka-c10647ef95e5)
	* [Load Balancing at Yelp](https://engineeringblog.yelp.com/2017/05/taking-zero-downtime-load-balancing-even-further.html)
	* [Load Balancing at Github](https://githubengineering.com/introducing-glb/)
	* [Consistent Hashing to Improve Load Balancing at Vimeo](https://medium.com/vimeo-engineering-blog/improving-load-balancing-with-a-new-consistent-hashing-algorithm-9f1bd75709ed)
	* [UDP Load Balancing at 500 pixel](https://developers.500px.com/udp-load-balancing-with-keepalived-167382d7ad08)
* [Parallel Computing](https://blogs.msdn.microsoft.com/ddperf/2009/05/02/are-we-taking-advantage-of-parallelism/)
	* [SPMD (Single Program Multiple Data): The Genetic Pattern](https://www2.eecs.berkeley.edu/Pubs/TechRpts/2012/EECS-2012-186.html)
	* [Master/Worker Pattern](https://docs.gigaspaces.com/sbp/master-worker-pattern.html)
	* [Loop Parallelism Pattern: Extracting parallel tasks from loops](https://www.cs.umd.edu/class/fall2001/cmsc411/projects/unroll/main.htm)
	* [Fork/Join Pattern: Good for recursive data processing](http://highscalability.com/learn-how-exploit-multiple-cores-better-performance-and-scalability)
	* [MapReduce Pattern: Born for Big Data](http://static.googleusercontent.com/media/research.google.com/en/us/archive/mapreduce-osdi04.pdf)
	* [Parallelize the rendering of web pages: Use case of Yelp.com](https://engineeringblog.yelp.com/2017/07/generating-web-pages-in-parallel-with-pagelets.html)
* [Distributed Machine Learning](https://arxiv.org/pdf/1512.09295.pdf)
	* [Scalable Deep Learning Platform On Spark In Baidu](https://www.slideshare.net/JenAman/scalable-deep-learning-platform-on-spark-in-baidu)
	* [Horovod: Uber’s Open Source Distributed Deep Learning Framework for TensorFlow](https://eng.uber.com/horovod/)	
	* [Scaling Gradient Boosted Trees for Click-Through-Rate Prediction at Yelp](https://engineeringblog.yelp.com/2018/01/building-a-distributed-ml-pipeline-part1.html)
	* [TensorFlowOnSpark: Distributed Deep Learning on Big Data Clusters at Yahoo](https://yahooeng.tumblr.com/post/157196488076/open-sourcing-tensorflowonspark-distributed-deep)
	* [CaffeOnSpark: Distributed Deep Learning on Big Data Clusters at Yahoo](https://yahooeng.tumblr.com/post/139916828451/caffeonspark-open-sourced-for-distributed-deep)

## Availability
* [Fail-over](https://activemq.apache.org/artemis/docs/1.0.0/ha.html)
* [Replication](https://m.alphasights.com/a-primer-on-database-replication-381b319cd032)
	* [Master-Slave](https://engineering.bitnami.com/articles/enabling-additional-nodes-to-bitnami-mysql-with-replication.html)
	* [Tree Replication](https://link.springer.com/chapter/10.1007/3-540-44863-2_47)
	* [Master-Master](http://sabbour.me/highly-available-and-scalable-master-master-mysql-on-azure-virtual-machines/)
	* [Buddy Replication](https://developer.jboss.org/wiki/JBossCacheBuddyReplicationDesign)
* [NodeJS High Availability at Yahoo](https://yahooeng.tumblr.com/post/68823943185/nodejs-high-availability)
* [Every Day Is Monday in Operations - LinkedIn (11 part series)](https://www.linkedin.com/pulse/introduction-every-day-monday-operations-benjamin-purgason)
* [Practical Guide to Monitoring and Alerting with Time Series at Scale](https://www.usenix.org/conference/srecon17americas/program/presentation/wilkinson)
* [How Robust Monitoring Powers High Availability for LinkedIn Feed](https://www.usenix.org/conference/srecon17americas/program/presentation/barot)

## Stability
* [Circuit Breaker](https://doc.akka.io/docs/akka/current/common/circuitbreaker.html)
* [Always use timeouts (if possible)](https://www.javaworld.com/article/2824163/application-performance/stability-patterns-applied-in-a-restful-architecture.html)
* [Let it crash/Supervisors: Embrace failure as a natural state in the life-cycle of the application](http://erlang.org/doc/design_principles/sup_princ.html)
* [Crash early: An error now is better than a response tomorrow](http://odino.org/better-performance-the-case-for-timeouts/)
* [Bulkheads: Partition and tolerate failure in one part](https://skife.org/architecture/fault-tolerance/2009/12/31/bulkheads.html)
* [Steady state: Always put logs on separate disk](https://docs.microsoft.com/en-us/sql/relational-databases/policy-based-management/place-data-and-log-files-on-separate-drives)
* [Throttling: Maintain a steady pace](http://www.sosp.org/2001/papers/welsh.pdf)
* [Multi-clustering: Improving Resiliency and Stability of a Large-scale Monolithic API Service at LinkedIn](https://engineering.linkedin.com/blog/2017/11/improving-resiliency-and-stability-of-a-large-scale-api)

## Others
* [Distributed Git server at Palantir](https://medium.com/@palantir/stemma-distributed-git-server-70afbca0fc29)
* [Configuration management for distributed systems (using GitHub and cfg4j) at Flickr](https://code.flickr.net/2016/03/24/configuration-management-for-distributed-systems-using-github-and-cfg4j/)
* [Seagull: Distributed system that helps running > 20 million tests per day at Yelp](https://engineeringblog.yelp.com/2017/04/how-yelp-runs-millions-of-tests-every-day.html)
* [Cloud Bouncer: Distributed Rate Limiting at Yahoo](https://yahooeng.tumblr.com/post/111288877956/cloud-bouncer-distributed-rate-limiting-at-yahoo)
* [Scalable gaming patterns on AWS (Sep 2017)](https://d0.awsstatic.com/whitepapers/aws-scalable-gaming-patterns.pdf)
* [Building a modern bank backend at Monzo](https://monzo.com/blog/2016/09/19/building-a-modern-bank-backend/)
* [Selecting a cloud provider at Etsy](https://codeascraft.com/2018/01/04/selecting-a-cloud-provider/)
* [Architecture of Tripod (Flickr’s Backend)](https://yahooeng.tumblr.com/post/157200523046/introducing-tripod-flickrs-backend-refactored)
* [How eBay's Shopping Cart used compression techniques to solve network I/O bottlenecks](https://www.ebayinc.com/stories/blogs/tech/how-ebays-shopping-cart-used-compression-techniques-to-solve-network-io-bottlenecks/)
* [Optimizing web servers for high throughput and low latency at Dropbox](https://blogs.dropbox.com/tech/2017/09/optimizing-web-servers-for-high-throughput-and-low-latency/)

## Books
* [The Art of Scalability](http://theartofscalability.com/)
* [Designing Data-Intensive Applications](https://dataintensive.net/)
* [Web Scalability for Startup Engineers](https://www.goodreads.com/book/show/23615147-web-scalability-for-startup-engineers)
* [Scalability Rules: 50 Principles for Scaling Web Sites](http://scalabilityrules.com/)

## Talks
* [Harvard CS75 - Lecture 9: Scalability](https://www.youtube.com/watch?v=-W9F__D3oY4)
* [How We've Scaled Dropbox - Kevin Modzelewski, Back-end Engineer at Dropbox](https://www.youtube.com/watch?v=PE4gwstWhmc)
* [Lessons of Scale at Facebook - Bobby Johnson, Director of Engineering at Facebook](https://www.youtube.com/watch?v=QCHiNEw73AU)
* [Scaling Instagram Infrastructure - Lisa Guo, Instagram Engineering](https://www.youtube.com/watch?v=hnpzNAPiC0E)
* [Scaling Twitter Core Infrastructure - Yao Yue, Staff Software Engineer at Twitter](https://www.youtube.com/watch?v=6OvrFkLSoZ0)
* [Scaling Pinterest - Marty Weiner, Pinterest’s founding engineer](https://www.youtube.com/watch?v=jQNCuD_hxdQ&list=RDhnpzNAPiC0E&index=11)
* [Scaling Spotify Data Infrastructure - Matti (Lepistö) Pehrs, Spotify](https://www.youtube.com/watch?v=cdsfRXr9pJU)
* [Designing for Failure: Scaling Uber's Backend by Breaking Everything - Matt Ranney, Chief Systems Architect at Uber](https://www.youtube.com/watch?v=nuiLcWE8sPA)
* [Netflix Guide to Microservices - Josh Evans, Director of Operations Engineering at Netflix](https://www.youtube.com/watch?v=CZ3wIuvmHeM&t=2837s)
* [Achieving Rapid Response Times in Large Online Services - Jeff Dean, Google Senior Fellow](https://www.youtube.com/watch?v=1-3Ahy7Fxsc)

## Special Thanks
* Jonas Bonér, CTO at Lightbend, for the [original inspiration](https://www.slideshare.net/jboner/scalability-availability-stability-patterns)

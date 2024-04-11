elk主要功能：将mysql中的数据同步至elasticsearch


而启动elk需要修改的地方在本问中只有两大块：
1：docker-compose.yaml文件中的“volumes”
将其中的文件路径改为您本机中到elk文件夹的路径。
例如： - /Users/yanlihong/Go/src/getHomeType/elk/elasticsearch/plugins:/usr/share/elasticsearch/plugins
其中的/Users/yanlihong/Go/src/getHomeType/elk就是我本机到elk文件夹的绝对路径。
（所有的都需要修改）


2：既然主要作用是同步，所以我们需要连接数据库。
而起到连接作用的是logstash，所以我们需要修改logstash里面的内容。
（只修改你想连接的数据库的部分）
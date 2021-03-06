### CentOS 6/7

1. Installation:

    Add the following in your `/etc/yum.repos.d/` directory in a file named (for example) `kong.repo`

    ```
    [kong]
    name = Kong
    baseurl = http://mashape-kong-yum-repo.s3-website-us-east-1.amazonaws.com/$releasever/$basearch
    enabled = 1
    gpgcheck = 0
    ```

    Then execute:

    ```bash
    yum install kong
    ```

2. Start Kong:

    Before starting Kong, make sure [Cassandra v2.1.3](http://cassandra.apache.org/) is running and [`kong.yml`](/docs/getting-started/configuration/) points to the right Cassandra server. Then execute:

    ```bash
    kong start
    ```

3. Kong is running:

    ```bash
    curl http://127.0.0.1:8001
    ```

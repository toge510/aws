# Tutorial1: Static Web Server

<img src=./arch1.png>

* VPC
* Security Group
  * Inbound rules
    * ssh
    * http
    * https
* Key-Pair
  * import public key of my homelab
* EC2
  * ssh ec2-user@< DNS name >
  * install nginx
    ```
    sudo amazon-linux-extras install nginx1 -y
    sudo systemctl enable --now nginx
    ```
* Target Group
  * target type: instance
  * select target instance
  * instance port: 80
* ELB (ALB)
  * check with editing `/usr/share/nginx/html/index.html` file.
* Route53
  * host zone
  * record
  * endpoint: ALB
  * `nslookup -type=NS toge510test.site`
* https
  * https://shigeo-t.hatenablog.com/entry/2021/07/09/050000
  * https://business.ntt-east.co.jp/content/cloudsolution/column-63.html
  * https://dev.classmethod.jp/articles/tsnote-acm-dns-validation-cname-check/
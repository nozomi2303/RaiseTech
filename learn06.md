# 課題6
  
### CloudTrailのログからイベントを確認する。  
  
CloudWatchアラームでメール通知設定した際のログ  
* "eventName":"DescribeAlarms"  
* "eventSource":"monitoring.amazonaws.com"  
* "eventCategory":"Management"  
* "eventType":"AwsApiCall"  




### CloudWatchアラーム通知設定をする。  

* Amazon SNSを設定する。  
![awssns](images/awssns.png)  

* 対象をALBに、UnHealthyHostCount/300秒辺りに1以上のアクセスがOKの場合とNGの場合にメールを送信する設定を行った。  
![alb-action-1](images/alb-action-1.png)  
![alb-action-2](images/alb-action-2.png)  

    * アクセスがOKの場合  
![alb-ok-console](images/alb-ok-console.png)  
![alb-ok-mail](images/alb-ok-mail.png)  
    * NGの場合  
![alb-alarm-console](images/alb-alarm-console.png)  
![alb-alarm-mail](images/alb-alarm-mail.png)  




### AWS見積書を作成する。  

* 今日までの課題に作ったリソースの見積書。  
    * VPC
    * EC2
    * RDS for MySQL
    * Elastic IP
    * ELB (ALB)
    * S3
    * CloudTrail
    * CloudWatch

<https://calculator.aws/#/estimate?id=b72ca9e818e2b6898ba968dfe58543895de8887f>  

* 6月のEC2請求額  
![ec2-cost](images/ec2-cost.png)  



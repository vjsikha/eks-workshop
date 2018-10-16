---
title: "Cleanup Scaling"
date: 2018-08-07T08:30:11-07:00
weight: 50
draft: true
---

```
kubectl delete -f ~/environment/cluster-autoscaler/ca_example.yaml
kubectl delete -f ~/environment/cluster-autoscaler/nginx.yaml
rm -rf ~/environment/cluster-autoscaler
aws iam delete-role-policy --role-name $ROLE_NAME --policy-name ASG-Policy-For-Worker
kubectl delete hpa,svc php-apache
kubectl delete svc php-apache
kubectl delete pods -l run
```
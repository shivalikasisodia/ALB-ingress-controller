* We are going to deploy all these 3 apps in kubernetes with context path based routing enabled in Ingress Controller
/app1/* - should go to app1-nginx-nodeport-service
/app2/* - should go to app1-nginx-nodeport-service
/* - should go to sermgmt-restapp-nodeport-service

* As part of this process, this respective annotation alb.ingress.   kubernetes.io/healthcheck-path: /usermgmt/health-status will be moved to respective application NodePort Service. Only generic settings will be present in Ingress manifest 
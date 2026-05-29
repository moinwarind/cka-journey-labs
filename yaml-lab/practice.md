apiVersion: v1
kind: pod
metadata:
  name: drill-three
  labels:
    app: web
    env: test
spec:
  containers: 
    - name: nginx
      image: nginx
      ports: 
        -containerport: 80
   

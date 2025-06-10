### test
Once deployed, get the Ingress IP:

'''
INGRESS_HOST=$(kubectl -n istio-system get svc istio-ingressgateway \
  -o jsonpath='{.status.loadBalancer.ingress[0].ip}')

curl http://$INGRESS_HOST
'''
'''
hey -z 30s -c 20 http://$INGRESS_HOST
'''
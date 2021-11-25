# cfk-openshift-aws-noble

NOTE: WORK IN PROGRESS

This is a set of development environment scripts to build Confluent Platform on OpenShift.

0. Create certs and secrets using ```mtls/cert-secrets.txt```
1. Start the brokers with ```kubectl apply -f brokers.yaml```
2. Setup the ACLs by logging into a kakfa broker pod, and copy paste the scripts from ```acls/acls.txt```
3. Start the CP services with ```kubectl apply -f services.yaml```
4. Add Rest Proxy ```helm upgrade --install kafka-rest-proxy cp-kafka-rest --set podSecurity.enabled=false -n confluent-ironbank```

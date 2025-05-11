apply:
	kubectl apply -f rbac.yaml
	kubectl apply -f clusterrolebinding.yaml
	kubectl delete configmap dozzle-auth
	kubectl create configmap dozzle-auth --from-file=users.yaml 
	kubectl apply -f deployment.yaml
	kubectl apply -f service.yaml

delete:
	kubectl delete -f service.yaml
	kubectl delete -f deployment.yaml
	kubectl delete configmap dozzle-auth
	kubectl delete -f clusterrolebinding.yaml
	kubectl delete -f rbac.yaml
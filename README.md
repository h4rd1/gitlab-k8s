kubectl exec -it -n gitlab <pod-name> -- grep 'Password:' /etc/gitlab/initial_root_password
#PASSWORD

gitlab runner 

kubectl run -it runner-registrator \
  --image=gitlab/gitlab-runner:latest \
  --restart=Never \
  -- register




kubectl create namespace gitlab


 storageClassName: local-storage # или оставьте пустым local-path

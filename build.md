For testing on local:
```
docker build --build-arg=FRAPPE_PATH=https://github.com/frappe/frappe --build-arg=FRAPPE_BRANCH=version-14 --build-arg=PYTHON_VERSION=3.10.5 --build-arg=NODE_VERSION=16.18.0  --tag=ducntq/erpnext:latest --file=images/custom/Containerfile .
```

For production build to zest repository:
```
docker buildx build --platform linux/amd64 --push -t registry.zest.win/erpnext-hrms --build-arg=FRAPPE_PATH=https://github.com/frappe/frappe --build-arg=FRAPPE_BRANCH=version-14 --build-arg=PYTHON_VERSION=3.10.5 --build-arg=NODE_VERSION=16.18.0 --file=images/custom/Containerfile .
```
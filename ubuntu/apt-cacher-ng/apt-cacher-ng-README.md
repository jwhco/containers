# Apt-Catcher-NG Proxy Container


## Configuration

Each client pod that requires caching needs following environment variable to point to the apt-cacher-ng service:


```yaml
env:
- name: APT_PROXY
  value: "http://apt-cacher-ng-service:3142"
  ```



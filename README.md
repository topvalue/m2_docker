## Docker Hub

View Dockerfiles:

- [markoshust/magento-nginx (Docker Hub)](https://hub.docker.com/r/markoshust/magento-nginx/)
  - 1.13
      - [`latest`, `1.13`, `1.13-7`](https://github.com/markshust/docker-magento/tree/master/images/nginx/1.13)
      - [`1.13-6`](https://github.com/markshust/docker-magento/tree/20.1.1/images/nginx/1.13)
      - [`1.13-5`](https://github.com/markshust/docker-magento/tree/18.1.1/images/nginx/1.13)
      - [`1.13-4`](https://github.com/markshust/docker-magento/tree/18.0.1/images/nginx/1.13)
      - [`1.13-3`](https://github.com/markshust/docker-magento/tree/15.0.1/images/nginx/1.13)
      - [`1.13-2`](https://github.com/markshust/docker-magento/tree/12.0.0/images/nginx/1.13)
      - [`1.13-1`](https://github.com/markshust/docker-magento/tree/11.1.5/images/nginx/1.13)
      - [`1.13-0`](https://github.com/markshust/docker-magento/tree/11.0.0/images/nginx/1.13)
- [markoshust/magento-php (Docker Hub)](https://hub.docker.com/r/markoshust/magento-php/)
  - 7.3
      - [`latest`, `7.3-fpm`, `7.3-fpm-0`](https://github.com/markshust/docker-magento/tree/master/images/php/7.3)
  - 7.2
      - [`7.2-fpm`, `7.2-fpm-3`](https://github.com/markshust/docker-magento/tree/master/images/php/7.2)
      - [`7.2-fpm-2`](https://github.com/markshust/docker-magento/tree/23.2.1/images/php/7.2)
      - [`7.2-fpm-1`](https://github.com/markshust/docker-magento/tree/23.1.1/images/php/7.2)
      - [`7.2-fpm-0`](https://github.com/markshust/docker-magento/tree/23.0.0/images/php/7.2)
  - 7.1
      - [`7.1-fpm`, `7.1-fpm-12`](https://github.com/markshust/docker-magento/tree/master/images/php/7.1)
      - [`7.1-fpm-11`](https://github.com/markshust/docker-magento/tree/23.2.1/images/php/7.1)
      - [`7.1-fpm-10`](https://github.com/markshust/docker-magento/tree/23.1.1/images/php/7.1)
      - [`7.1-fpm-9`](https://github.com/markshust/docker-magento/tree/23.0.0/images/php/7.1)
      - [`7.1-fpm-8`](https://github.com/markshust/docker-magento/tree/17.0.1/images/php/7.1)
      - [`7.1-fpm-7`](https://github.com/markshust/docker-magento/tree/16.2.0/images/php/7.1)
      - [`7.1-fpm-6`](https://github.com/markshust/docker-magento/tree/16.0.0/images/php/7.1)
      - [`7.1-fpm-5`](https://github.com/markshust/docker-magento/tree/15.0.1/images/php/7.1)
      - [`7.1-fpm-4`](https://github.com/markshust/docker-magento/tree/15.0.0/images/php/7.1)
      - [`7.1-fpm-3`](https://github.com/markshust/docker-magento/tree/14.0.1/images/php/7.1)
      - [`7.1-fpm-2`](https://github.com/markshust/docker-magento/tree/13.0.0/images/php/7.1)
      - [`7.1-fpm-1`](https://github.com/markshust/docker-magento/tree/11.1.5/images/php/7.1)
      - [`7.1-fpm-0`](https://github.com/markshust/docker-magento/tree/11.0.0/images/php/7.1)
- [markoshust/magento-elasticsearch (Docker Hub)](https://hub.docker.com/r/markoshust/magento-elasticsearch/)
  - 6.5
      - [`latest`, `6.5`, `6.5.4-0`](https://github.com/markshust/docker-magento/tree/master/images/elasticsearch/6.5)

## Setup

### Automated Setup (New Project)

> macOS & Linux Only

Run this automated one-liner from the directory you want to install your project to:

```bash
curl -s https://raw.githubusercontent.com/topvalue/m2_docker/master/lib/onelinesetup?token=AB5MMZ3Z75GSQHLH5VL5UBK5VSIRG | bash -s -- magento2.test 2.3.3
```

With Example Data
```bash
curl -s https://raw.githubusercontent.com/topvalue/m2_docker/master/lib/onelinesetup?token=AB5MMZ3Z75GSQHLH5VL5UBK5VSIRG | bash -s -- magento2.test with-samples-2.3.3



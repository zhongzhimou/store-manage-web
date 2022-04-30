# 骆驼门店仓库管理系统

## Build Setup

```bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```

For detailed explanation on how things work, check out the [documentation](https://www.nuxtjs.cn/).

## 部署

npm run generate

### nginx

location /storemanage {
        alias   /code/dist/; // 代码目录当前 dist
        try_files $uri.html $uri/index.html $uri;
        index  index.html index.htm;
}

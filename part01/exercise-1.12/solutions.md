```
❯ docker build -t frontend .
Sending build context to Docker daemon  729.1kB
Step 1/11 : FROM ubuntu:18.04
 ---> 3941d3b032a8
Step 2/11 : WORKDIR /usr/app/src
 ---> Using cache
 ---> 70d94cfa9ac7
Step 3/11 : EXPOSE 5000
 ---> Using cache
 ---> a1a00a434ac6
Step 4/11 : RUN apt-get update && apt-get install -y curl
 ---> Using cache
 ---> b993762251a0
Step 5/11 : RUN curl -sL https://deb.nodesource.com/setup_16.x | bash
 ---> Using cache
 ---> f355c435781f
Step 6/11 : RUN apt install -y nodejs
 ---> Using cache
 ---> 3d83ce3d4110
Step 7/11 : COPY . .
 ---> 3d93e02451c8
Step 8/11 : RUN npm install
 ---> Running in 0f663b4324a1
npm WARN old lockfile 
npm WARN old lockfile The package-lock.json file was created with an old version of npm,
npm WARN old lockfile so supplemental metadata must be fetched from the registry.
npm WARN old lockfile 
npm WARN old lockfile This is a one-time fix-up, please be patient...
npm WARN old lockfile 
npm WARN deprecated w3c-hr-time@1.0.2: Use your platform's native performance.now() and performance.timeOrigin.
npm WARN deprecated urix@0.1.0: Please see https://github.com/lydell/urix#deprecated
npm WARN deprecated stable@0.1.8: Modern JS already guarantees Array#sort() is a stable sort, so this library is deprecated. See the compatibility table on MDN: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/sort#browser_compatibility
npm WARN deprecated sourcemap-codec@1.4.8: Please use @jridgewell/sourcemap-codec instead
npm WARN deprecated source-map-url@0.4.0: See https://github.com/lydell/source-map-url#deprecated
npm WARN deprecated source-map-resolve@0.5.3: See https://github.com/lydell/source-map-resolve#deprecated
npm WARN deprecated sane@4.1.0: some dependency vulnerabilities fixed, support for node < 10 dropped, and newer ECMAScript syntax/features added
npm WARN deprecated rollup-plugin-terser@5.3.1: This package has been deprecated and is no longer maintained. Please use @rollup/plugin-terser
npm WARN deprecated svgo@1.3.2: This SVGO version is no longer supported. Upgrade to v2.x.x.
npm WARN deprecated rollup-plugin-babel@4.4.0: This package has been deprecated and is no longer maintained. Please use @rollup/plugin-babel.
npm WARN deprecated resolve-url@0.2.1: https://github.com/lydell/resolve-url#deprecated
npm WARN deprecated request-promise-native@1.0.9: request-promise-native has been deprecated because it extends the now deprecated request package, see https://github.com/request/request/issues/3142
npm WARN deprecated querystring@0.2.0: The querystring API is considered Legacy. new code should use the URLSearchParams API instead.
npm WARN deprecated request@2.88.2: request has been deprecated, see https://github.com/request/request/issues/3142
npm WARN deprecated har-validator@5.1.5: this library is no longer supported
npm WARN deprecated flatten@1.0.3: flatten is deprecated in favor of utility frameworks such as lodash.
npm WARN deprecated babel-eslint@10.1.0: babel-eslint is now @babel/eslint-parser. This package will no longer receive updates.
npm WARN deprecated axios@0.21.0: Critical security vulnerability fixed in v0.21.1. For more information, see https://github.com/axios/axios/pull/3410
npm WARN deprecated core-js@3.8.1: core-js@<3.23.3 is no longer maintained and not recommended for usage due to the number of issues. Because of the V8 engine whims, feature detection in old core-js versions could cause a slowdown up to 100x even if nothing is polyfilled. Some versions have web compatibility issues. Please, upgrade your dependencies to the actual version of core-js.
npm WARN deprecated core-js-pure@3.8.1: core-js-pure@<3.23.3 is no longer maintained and not recommended for usage due to the number of issues. Because of the V8 engine whims, feature detection in old core-js versions could cause a slowdown up to 100x even if nothing is polyfilled. Some versions have web compatibility issues. Please, upgrade your dependencies to the actual version of core-js-pure.
npm WARN deprecated @npmcli/move-file@1.0.1: This functionality has been moved to @npmcli/fs
npm WARN deprecated @material-ui/system@4.11.2: You can now upgrade to @mui/system. See the guide: https://mui.com/guides/migration-v4/
npm WARN deprecated @material-ui/styles@4.11.2: Material UI v4 doesn't receive active development since September 2021. See the guide https://mui.com/material-ui/migration/migration-v4/ to upgrade to v5.
npm WARN deprecated @hapi/topo@3.1.6: This version has been deprecated and is no longer supported or maintained
npm WARN deprecated @hapi/joi@15.1.1: Switch to 'npm install joi'
npm WARN deprecated @hapi/hoek@8.5.1: This version has been deprecated and is no longer supported or maintained
npm WARN deprecated @hapi/bourne@1.3.2: This version has been deprecated and is no longer supported or maintained
npm WARN deprecated @hapi/address@2.1.4: Moved to 'npm install @sideway/address'
npm WARN deprecated @material-ui/core@4.11.2: Material UI v4 doesn't receive active development since September 2021. See the guide https://mui.com/material-ui/migration/migration-v4/ to upgrade to v5.
npm WARN deprecated @material-ui/icons@4.11.2: You can now upgrade to @mui/icons. See the guide: https://mui.com/guides/migration-v4/
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm WARN deprecated chokidar@2.1.8: Chokidar 2 does not receive security updates since 2019. Upgrade to chokidar 3 with 15x fewer dependencies
npm WARN deprecated chokidar@2.1.8: Chokidar 2 does not receive security updates since 2019. Upgrade to chokidar 3 with 15x fewer dependencies
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm WARN deprecated core-js@2.6.12: core-js@<3.23.3 is no longer maintained and not recommended for usage due to the number of issues. Because of the V8 engine whims, feature detection in old core-js versions could cause a slowdown up to 100x even if nothing is polyfilled. Some versions have web compatibility issues. Please, upgrade your dependencies to the actual version of core-js.

added 1943 packages, and audited 1944 packages in 3m

125 packages are looking for funding
  run `npm fund` for details

63 vulnerabilities (1 low, 13 moderate, 34 high, 15 critical)

To address issues that do not require attention, run:
  npm audit fix

To address all issues (including breaking changes), run:
  npm audit fix --force

Run `npm audit` for details.
npm notice 
npm notice New major version of npm available! 8.19.4 -> 9.6.6
npm notice Changelog: <https://github.com/npm/cli/releases/tag/v9.6.6>
npm notice Run `npm install -g npm@9.6.6` to update!
npm notice 
Removing intermediate container 0f663b4324a1
 ---> 30b3fe746816
Step 9/11 : RUN npm run build
 ---> Running in 63cc364e0a5d

> example-frontend@0.1.0 build
> react-scripts build

(node:27) [DEP0148] DeprecationWarning: Use of deprecated folder mapping "./" in the "exports" field module resolution of the package at /usr/app/src/node_modules/postcss-safe-parser/node_modules/postcss/package.json.
Update this package.json to use a subpath pattern like "./*".
(Use `node --trace-deprecation ...` to show where the warning was created)
Creating an optimized production build...
Browserslist: caniuse-lite is outdated. Please run:
npx browserslist@latest --update-db

Why you should do it regularly:
https://github.com/browserslist/browserslist#browsers-data-updating
Compiled successfully.

File sizes after gzip:

  77.24 KB  build/static/js/2.43ca3586.chunk.js
  1.91 KB   build/static/js/main.287280c9.chunk.js
  781 B     build/static/js/runtime-main.223e45fb.js
  235 B     build/static/css/main.eaa5d75e.chunk.css

The project was built assuming it is hosted at /.
You can control this with the homepage field in your package.json.

The build folder is ready to be deployed.
You may serve it with a static server:

  npm install -g serve
  serve -s build

Find out more about deployment here:

  https://cra.link/deployment

Removing intermediate container 63cc364e0a5d
 ---> 451f89fe3d98
Step 10/11 : RUN npm install -g serve
 ---> Running in 963fac3d0619

added 89 packages, and audited 90 packages in 10s

24 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
Removing intermediate container 963fac3d0619
 ---> b5142f925466
Step 11/11 : CMD ["serve","-s","-l","5000","build"]
 ---> Running in db44b81234b3
Removing intermediate container db44b81234b3
 ---> 3f9b0e7af5ea
Successfully built 3f9b0e7af5ea
Successfully tagged frontend:latest

❯ docker run -p 5000:5000 frontend
 INFO  Accepting connections at http://localhost:5000
 HTTP  5/6/2023 6:05:10 AM 172.17.0.1 GET /
 HTTP  5/6/2023 6:05:10 AM 172.17.0.1 Returned 200 in 346 ms
 HTTP  5/6/2023 6:05:10 AM 172.17.0.1 GET /static/css/main.eaa5d75e.chunk.css
 HTTP  5/6/2023 6:05:10 AM 172.17.0.1 GET /static/js/2.43ca3586.chunk.js
 HTTP  5/6/2023 6:05:10 AM 172.17.0.1 GET /static/js/main.287280c9.chunk.js
 HTTP  5/6/2023 6:05:10 AM 172.17.0.1 Returned 200 in 8 ms
 HTTP  5/6/2023 6:05:10 AM 172.17.0.1 Returned 200 in 9 ms
 HTTP  5/6/2023 6:05:10 AM 172.17.0.1 Returned 200 in 18 ms
 HTTP  5/6/2023 6:05:10 AM 172.17.0.1 GET /static/media/toskalogo.c0f35cf0.svg
 HTTP  5/6/2023 6:05:10 AM 172.17.0.1 Returned 200 in 3 ms
 HTTP  5/6/2023 6:05:10 AM 172.17.0.1 GET /favicon.ico
 HTTP  5/6/2023 6:05:10 AM 172.17.0.1 Returned 200 in 2 ms
 ```
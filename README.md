# vs2017-angular4-kit-starter

#The difference between the two kit (ng2 & ng4)

|   |   |   |   |
|---|:-:|:-:|:-:|
| packages name   |  kit ng2 |    | kit ng4  |
| @angular/common|                        ^2.4.10|   →       |^4.0.0-rc.5|
| @angular/compiler|                      ^2.4.10|   →       |^4.0.0-rc.5|
| @angular/core|                          ^2.4.10|   →       |^4.0.0-rc.5|
| @angular/forms|                         ^2.4.10|   →       |^4.0.0-rc.5|
| @angular/http|                          ^2.4.10|   →       |^4.0.0-rc.5|
| @angular/platform-browser|              ^2.4.10|   →       |^4.0.0-rc.5|
| @angular/platform-browser-dynamic|      ^2.4.10|   →       |^4.0.0-rc.5|
| @angular/platform-server|               ^2.4.10|   →       |^4.0.0-rc.5|
| @angular/router|                        ^3.4.10|   →       |^4.0.0-rc.5|
  
# ng2 is working
# ng4 is have error https://github.com/angular/angular/issues/15332

```
ERROR in [at-loader] ./node_modules/angular2-platform-node/node-platform.d.ts:1:10 
TS2305: Module '"C:/dotnet-aspnet-core-angular/node_modules/@angular/platform-browser/platform-browser"' has no exported member 'AnimationDriver'.

ERROR in [at-loader] ./node_modules/angular2-platform-node/node-renderer.d.ts:2:10 
TS2305: Module '"C:/dotnet-aspnet-core-angular/node_modules/@angular/platform-browser/platform-browser"' has no exported member 'AnimationDriver'.
```

#Minimal reproduction of the problem with instructions

## clonning or ....

1) instal VS2017 Comunity and node 7.7.3
2) instal in terminal `PS> dotnet new --install Microsoft.AspNetCore.SpaTemplates::* `
3) crate new in terminal `PS> dotnet new angular`
4) instal in terminal `npm i -g npm-upgrade` or `yarn global add npm-upgrade`
5) upgrade in terminal `npm-upgrade`
.) next open `package.json` and change `angular` from `2.4.10` to `4.0.0-rc.5`
6) in terminal `npm install` or `yarn`
7) open project in VS2017 and start compiling


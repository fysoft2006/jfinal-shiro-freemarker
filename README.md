jfinal-shiro-freemarker
============

jfinal  shiro plugin  freemarker tags

已经登陆判断
```html
<@shiro.authenticated>
  <li><a href="/user/center"><@shiro.principal name="full_name"/></a></li>
      |
  <li><a href="/signout">退出</a></li>
</@shiro.authenticated>

```

没有登陆判断
```html

<@shiro.notAuthenticated>
  <li><a href="/">登陆</a></li>
</@shiro.notAuthenticated>

```

显示登陆异常

```html

<@shiro.isLoginFailure name="shiroLoginFailure">
  <@shiro.loginException name="shiroLoginFailure"/>
</@shiro.isLoginFailure>

```
判断角色
```html
<@shiro.hasRole name="ROLE_ADMIN">
我是admin
</@shiro.hasRole>

```

判断权限

```html

<@shiro.hasPermission name="P_ORDER_CONTROL">
  <li><a href="/order/branch" class="<#if activebar=='branch'>nav-active</#if>">全部订单</a></li>
</@shiro.hasPermission>

```



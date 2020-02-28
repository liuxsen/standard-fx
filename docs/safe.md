# 安全守则

1. 不要相信url，使用[sanitize-url](https://www.npmjs.com/package/@braintree/sanitize-url)处理url，渲染dom
2. HTTP-only Cookie: 禁止 JavaScript 读取某些敏感 Cookie，攻击者完成 XSS 注入后也无法窃取此 Cookie。
3. 不要使用 DOM 中的内联事件监听器,使用vue自己的事件代理触发事件location、onclick、onerror、onload、onmouseover 等，
4. 禁止使用eval
5. 谨慎处理不可信数据，作为标签属性，如a标签的 href 属性
6. 输入内容长度控制
   1. 对于不受信任的输入，都应该限定一个合理的长度。虽然无法完全防止 XSS 发生，但可以增加 XSS 攻击的难度。
7. 使用https，并且http重定向到https
8. html模板加csp(内容安全策略)标签 TODO
9. reffer限制，非本站域名，禁止访问

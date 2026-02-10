metaLinks:
  alternates:
    - /broken/spaces/pt4moEMpSf4BGvjJCzQm/pages/1yx4GJhhoYrra0NzZTb8
---

# 注意事项

### 市场测试的检查模式绕行方案

#### 基本政策

LINE NEXT完成市场设置及开通后，将在市场开放前保持检查模式以阻止外部访问。游戏开发商可使用LINE NEXT提供的检查模式绕行URL进行访问。如需确认检查模式绕行URL，请向负责人提出申请。

#### 通过Webview进行测试时

在API请求时，请在请求头中添加可从维护绕行URL获取的Cookie值。

```
key: MAINTENANNCE_COOKIE
value: xxxxxxx-....
```

若维护绕行URL变更，value也可能随之改变，因此需采用运行时动态配置方案。

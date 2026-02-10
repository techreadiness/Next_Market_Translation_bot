metaLinks:
  alternates:
    - /broken/spaces/pt4moEMpSf4BGvjJCzQm/pages/1yx4GJhhoYrra0NzZTb8
---

# Notes

### Workaround for Market Testing

#### Default Policy

Once LINE NEXT completes Market setup and launch, it remains in maintenance mode until the official Market opening, preventing external access. Game developers can access it using the maintenance bypass URL provided by LINE NEXT. If you need to confirm the maintenance bypass URL, please request it from your assigned contact.

#### For Testing via Webview

When making API requests, add the Cookie value found in the bypass URL to the header.

```
key: MAINTENANNCE_COOKIE
value: xxxxxxx-....
```

The value may change if the bypass URL is updated, so runtime configuration is required.

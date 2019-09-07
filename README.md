### LanguageClient-neovim
---
https://github.com/autozimu/LanguageClient-neovim

```rs
// src/language_server_protocol.rs

impl LanguageClient {
  pub fn get_client(&self, lang_id: &LanguageId) -> Fallible<RpcClient> {
    self.get(|state| state.clients.get(lang_id).cloned())?
      .ok_or_else(|| {
        LCError::ServerNotRunning {
          languageId: lang_id.clone().unwrap_or_default(),
        }
        .into()
      })
  }
  
  pub fn loop_call() {}
  
  fn sync_settings() -> Fallible<> {}
}
```

```
```

```
```


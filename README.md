# Setup CentOS 7

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/kubotan/motioneye/dev/setup)"
```

# 注意事項
- 写真を撮るボタンがマニュアル撮影でも表示されない場合は、ブラウザキャッシュを削除すること。
- ブラウザキャッシュ削除はCtrl + F5では改善できない。ブラウザ設定からキャッシュを完全に削除すること。
- 上記も表示されない場合はset_extra_headers直下に以下を埋め込むこと。
```patch
def set_extra_headers(self, path):
+    self.set_header("Cache-control", "no-cache")
```

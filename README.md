# CloudflareScan

一个 IP 扫描与测速工具（IPv4/IPv6），支持完全测速、分地区测速、导出结果。

## 本地运行

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
python cloudflarescan.txt
```

## 打包（PyInstaller）

```bash
pip install pyinstaller
pyinstaller --noconfirm --clean --windowed --onefile cloudflarescan.txt --name cloudflarescan
```

生成文件在 `dist/`。

## GitHub Actions 自动发布

推送 tag（例如 `v1.0.1`）后会自动在 Windows/macOS/Linux 打包，并在 Release 里上传附件。

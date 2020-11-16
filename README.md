### MacOS Terminal 使用 Touch ID 的方法：

Enable: `sudo sed -i ".bak" '2s/^/auth       sufficient     pam_tid.so\'$'\n/g' /etc/pam.d/sudo`

作法：在`/etc/pam.d/sudo`的第二行加入`auth       sufficient     pam_tid.so`

Disable: `sudo mv /etc/pam.d/sudo.bak /etc/pam.d/sudo`

作法：在`/etc/pam.d/sudo`的第二行移除`auth       sufficient     pam_tid.so`


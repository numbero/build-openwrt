
Target System ---> Arm System Ready (EFI) Compliant
Subtarget ---> 64-bit (armv8)

Target Images ---> VMDK
Target Images ---> (256) Kernel partition size (in MB)                  #默认是 (16) 建议修改 (256)
Target Images ---> (512) Root filesystem partition size (in MB)        #默认是 (160) 建议修改 (512)

## 支持ipv6
Extra packages  --->  ipv6helper

## 无线网卡驱动
Kernel Modules ---> wireless drivers ---> kmod-mt7921-firmware

## 主题
luci-theme-argon

## 应用
luci-app-argon-config
luci-app-ddnsgo
luci-app-dockerman
luci-app-openclash
luci-app-openvpn-server
luci-app-quickstart
luci-app-ttyd
luci-app-store

## 打开适用于VMware的VM Tools
## Utilities  --->  open-vm-tools  #打开适用于VMware的VM Tools
## Utilities  --->  open-vm-tools-fuse  #打开适用于VMware的VM Tools

## 如果是arm编译机 需要将以下配置替换
CONFIG_GOLANG_EXTERNAL_BOOTSTRAP_ROOT=""
### 更换为
CONFIG_GOLANG_EXTERNAL_BOOTSTRAP_ROOT="/opt/homebrew/Cellar/go/1.25.4/libexec"

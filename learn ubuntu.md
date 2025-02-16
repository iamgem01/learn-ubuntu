# [![My Skills](https://skillicons.dev/icons?i=linux&perline=3)](https://skillicons.dev) Learn-ubuntu 
## Fix language vie on ubuntu
- Mở terminal lên và gõ từng lệnh
  
`sudo add-apt-repository ppa:bamboo-engine/ibus-bamboo`

 `sudo apt-get update`
 
`sudo apt-get install ibus ibus-bamboo --install-recommends`

`ibus restart `

**Note**:Error:`ibus can't restart` thì `log out` và đăng nhập lại rồi nhập lệnh vào là được.

- Đặt ibus-bamboo làm bộ gõ mặc định

`env DCONF_PROFILE=ibus dconf write /desktop/ibus/general/preload-engines "['BambooUs', 'Bamboo']" && gsettings set org.gnome.desktop.input-sources sources "[('xkb', 'us'), ('ibus', 'Bamboo')]"`

- Nếu gặp lỗi thì có thể uninstall nó bằng lệnh:
  
`sudo apt-get remove ibus-bamboo –y`

`sudo apt-get autoremove –y`
  

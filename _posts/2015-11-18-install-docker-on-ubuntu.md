---
layout: post
subtitle: "在 Ubuntu 上安裝 Docker"
description: "剛灌好了一個 ubuntu Server 15.10 的空機。想說來試試用 Docker。"
tags: [how-to, docker, ubuntu]
---

# 前情提要

剛灌好了一個 ubuntu Server 15.10 的空機。想說來試試用 Docker。


# 安裝步驟

` # curl -sSL https://get.docker.com/ | sudo sh `

上面的指令會連線至 Docker 官網下載安裝指令碼執行。我們都不用動手。這樣就結束了!!!!


# 驗證步驟   

不信邪馬上打開來試試 

`# sudo docker run -i -t ubuntu /bin/bash`

執行 Ubuntu Docker 的映像檔，如果沒有下載過的話會下載。

如果正確的話會看到：

`root@04355750b494:/#`

發現提示符變了，就表示你已經裝好了。也太容易了點…


# 補充

* 如果要讓非root 帳號使用 docker ，需再執行 sudo usermod -aG docker managermanager 換成你的帳號即可。

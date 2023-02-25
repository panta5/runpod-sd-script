# Runpod SD-WebUI One Script Installer

## Getting started

**You need to use the PyTorch template (python3.10) in Runpod.**

* Download the startscript file

```bash
wget https://gist.github.com/panta5/8706ce687576c4a80192fa3c05cffafc/raw/runpod_sd_webui_startscript.sh -O /root/runpod_startscript.sh
```

* Modify the authtoken in the startscript.

> If your authtoken is *2LVuzCWgjGPQ94uEKJ4uEKJKVJy\_EKJKVJygjGPQ94ubvJW9Y* then enter it like this
>
> DO NOT MODIFY *NGROK_TOKEN_HERE*

```bash
sed -i 's/NGROK_TOKEN_HERE/2LVuzCWgjGPQ94uEKJ4uEKJKVJy_EKJKVJygjGPQ94ubvJW9Y/g' /root/runpod_startscript.sh
```

* Grant the startscript execution privileges

```bash
chmod +x /root/runpod_startscript.sh
```

* Run the startscript

```bash
bash /root/runpod_startscript.sh
```

* Wait until it says it's done, as shown below.

```
환경 구성이 완료됐습니다.
이후부터는 시작할 때 /workspace/stable-diffusion-webui/start.sh 파일을 실행해주세요
```

* Run the WebUI

```bash
bash /workspace/stable-diffusion-webui/start.sh
```

If you run it, you can see the Ngrok URL below.
Now enjoy it.

> Once it's installed, we'll only run it with the */workspace/stable-diffusion-webui/start.sh* file from now on.


## ㄹㅇ 한방설치 가이드

* *토큰여기다넣어* 부분만 본인 토큰으로 교체후 터미널에 복붙 ㄱㄱ

```bash
wget https://gist.github.com/panta5/8706ce687576c4a80192fa3c05cffafc/raw/runpod_sd_webui_startscript.sh -O /root/runpod.sh && chmod +x /root/runpod.sh && sed -i 's/NGROK_TOKEN_HERE/토큰여기다넣어/g' /root/runpod.sh && bash /root/runpod.sh
```

## 유의사항

* 유지보수는 내가 필요하면 할 예정임
* 한번만 설치해두면 다음부터는 */workspace/stable-diffusion-webui/start.sh* 만 켜면 자동으로 켜짐
* 스팟 인스턴스 호환용으로 만들긴 했는데 스팟에서 제대로 작동안될수도 있음
* PyTorch 템플릿 써야 제대로 작동될거임
* 구름도 될거같긴한데 파이썬 3.10 이랑 pip는 사전설치 해야된다는거!!


## Credit

1. https://github.com/AUTOMATIC1111/stable-diffusion-webui
2. https://stackoverflow.com/questions/238073/how-to-add-a-progress-bar-to-a-shell-script
3. https://stackoverflow.com/questions/27162552/how-to-run-ngrok-in-background
4. https://huggingface.co/Linaqruf/anything-v3.0/
5. https://huggingface.co/hakurei/waifu-diffusion-v1-4/
6. https://huggingface.co/datasets/gsdf/EasyNegative/
7. https://github.com/DominikDoom/a1111-sd-webui-tagcomplete

thx.

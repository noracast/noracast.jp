# noracast

[https://noracast.jp](https://noracast.jp)

# 音源ファイルの作り方

1. GarageBand  or Adboe Auditionで編集して書き出し
2. モノラル変換・圧縮
  ```sh
  ffmpeg -i stereo.mp3 -ac 1 mono.mp3
  ```
3. [Podcast Chapters](https://chaptersapp.com/)でチャプター付与（AACの場合は[Forecast](https://overcast.fm/forecast)が使える）
4. アップロード
  ```sh
  gsutil cp mono.mp3 gs://noracast
  ```

順番的に、[最後にffmpegを通すのが良さそう](https://gist.github.com/naokazuterada/5cb8798881a146faca790a2ff86415c7)だったが、チャプター情報が消えてしまうので、上記の順番にすること。

## deloyの仕方

- Staging: master
- Production: manual deploy on netlify

## misc 

- [リンク集](https://noraneers.slack.com/files/T3YLLA5FZ/FMWLUV63F?origin_team=T3YLLA5FZ)

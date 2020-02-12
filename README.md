# GoogleTranslateVoiceDownloader
Đoạn script này có thể giúp bạn tải lời thoại hàng loạt của "chị Google" từ [texttospeech.io](https://texttospeech.io).

English version [here](README-en.md)

This guide is targeted to **Vietnamese**. You can simply use [soundoftext](https://soundoftext.com) if you use a different language.

# Yêu cầu
* Python 3
* Các module cần thiết: requests, fake_useragent

# Cài đặt
* Download hoặc git clone repo này về máy của bạn.

# Hướng dẫn sử dụng
* Tạo 1 file tên *"input.txt"* trong cùng thư mục với script.
* Viết "kịch bản" của bạn (những lời thoại mà bạn muốn tải) vào file đó. Mỗi dòng sẽ được lưu thành một file *mp3* riêng biệt.
* Chạy *run.bat* nếu bạn dùng Windows hoặc *run.sh* nếu bạn dùng GNU/Linux. Bạn cũng có thể chạy trực tiếp file *.py* nhưng bạn sẽ không được thông báo kết quả (tải có thành công hay gặp lỗi ở đâu đó).
* Nếu được tải thành công, file mp3 sẽ được lưu trong thư mục *"downloaded"*.

# Config
* Bạn có thể cấu hình script với file *config.json* kèm theo, nhưng thường là không cần trừ khi bạn muốn vọc phá thứ gì đó, ví dụ như tải giọng của "chị Google" mới chẳng hạn.
    * `lang`: mã ngôn ngữ bằng 2 kí tự, và mã vùng nếu có (vd: vi, jp, ko, en-US, en-GB, ...). *(Mặc định: g1)*
    * `engine`: engine mà Google Dịch sử dụng. Thực ra mình cũng chẳng biết đây là cái gì. *(Mặc định: g1)*
        * Lưu ý đối với **tiếng Việt** : **engine = g1** sẽ tải **giọng cũ** (cái giọng vui vui mà bạn thường lấy trên mấy video meme), còn **engine = g2** sẽ tải **giọng mới** (giọng đang được sử dụng mặc định trên Google Dịch).
    * `rate`: Tốc độ của câu thoại *(Mặc định: 0.5)*.
    * `pitch`: Cao độ của giọng đọc (cao hay thấp) *(Mặc định: 0.5)*.
    * `gender`: the gender of the voice (male, female) *(Mặc định: female)*.
    * `wait`: Khoảng thời gian chờ giữa những lần download *(Mặc định: 0.5)*.

## Một số ví dụ cho khoá `lang`
| Language name       | `lang` key |
| ------------------- | ---------- |
| Vietnamese          | vi         |
| English (US)        | en-US      |
| English (GB)        | en-GB      |
| English (AU)        | en-AU      |
| Chinese (Simp)      | zh-CN      |
| Chinese (Hong Kong) | zh-HK      |
| Chinese (Taiwan)    | zh-TW      |
| Japanese            | ja         |
| Korean              | ko         |
| French              | fr         |

Trên đây chỉ là 1 số ví dụ điển hình. Nếu bạn biết mã (và mã vùng nếu có) của ngôn ngữ đó bạn hoàn toàn có thể gán nó cho khoá `lang` được cung cấp.

Thực tế nếu bạn muốn download hàng loạt bằng giọng của chị Google mới, hay của ngôn ngữ khác (vd như tiếng Anh), bạn có thể đơn giản sử dụng [soundoftext.com](https://soundoftext.com).
Nhưng script của mình tiện lợi hơn ở chỗ bạn có thể download hàng loạt mà không cần phải nhấn lần lượt từng nút download như trên soundoftext.com 🐧

Script của mình chỉ tải lại audio từ [texttospeech.io](https://texttospeech.io), mình không phải là chủ sở hữu của API này.
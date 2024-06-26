# รวมมิจ
## รวมสารพัดข้อมูลเพื่อช่วยให้คุณพ้นภัยจากมิจฉาชีพ

![cover.png](image%2Fcover.png)

แอปสำหรับตรวจสอบแอปที่น่าสงสัยภายในเครื่องที่สุ่มเสี่ยงต่อความปลอดภัยของผู้ใช้ในด้านต่าง ๆ เช่น แอปที่ถูกติดตั้งจากช่องทางที่ไม่ปลอดภัย หรือการใช้ Accessibility Services ในทางที่ไม่ถูกต้อง เป็นต้น

![highlight.png](image%2Fhighlight.png)

## ฟีเจอร์ที่มีให้ใช้งาน
* ตรวจสอบแอปที่ถูกติดตั้งจากช่องทางที่ไม่ปลอดภัย พร้อมกับแสดงข้อมูลสำคัญของแอปเพื่อช่วยให้ผู้ใช้ตรวจสอบแอปภายในเครื่องตัวเองได้ง่ายขึ้น
* ตรวจสอบแอปที่มีการใช้งานการเชื่อเหลือพิเศษหรือ Accessibility Service ภายในเครื่อง
* ตรวจสอบแอปที่กำลังจับภาพหน้าจออยู่ในขณะนั้น (Screen Sharing หรือ Media Projection)

## ความเป็นส่วนตัวของผู้ใช้
* แอปทำงานแบบออฟไลน์ ไม่ได้ขอสิทธิ์เข้าถึง Internet ตั้งแต่แรกเพื่อให้ผู้ใช้มั่นใจได้ว่าข้อมูลส่วนตัวของผู้ใช้จะไม่ถูกส่งออกไปที่อื่น [ตรวจสอบโค้ดได้ที่ [AndroidManifest.xml](app%2Fsrc%2Fmain%2FAndroidManifest.xml)]
* แอปขอสิทธิ์ (Permission) ที่เรียกว่า `QUERY_ALL_PACKAGES` ซึ่งเป็นสิทธิ์ในการขอค้นหาแอปที่ติดตั้งอยูภายในเครื่องเท่านั้น และเป็นแค่เพียงสิทธิ์เดียวเท่านั้นที่แอปที่ขอเข้าถึง และนั่นก็เป็นเหตุผลที่ทำให้แอปนี้ไม่สามารถอยู่บน Google Play ได้ เนื่องจากแอปนี้ไม่เข้าข่ายแอปที่จะใช้งานงานสิทธิ์ดังกล่าวได้
* ไม่มีการทำงานเบื้องหลังใด ๆ แอปจะทำงานในตอนที่ผู้ใช้เปิดใช้งานเท่านั้น
* ไม่มีการเก็บข้อมูลใด ๆ ของผู้ใช้ รวมไปถึงข้อมูลแอปที่ติดตั้งในเครื่องที่เราจะตรวจสอบใหม่ทุกครั้งเมื่อคุณเปิดแอปขึ้นมา
* ถ้าคุณรู้สึกว่าแอปดูเรียบง่าย และทำอะไรได้ไม่เยอะ นั่นสิ่งที่ทีมพัฒนาตั้งใจให้เป็นเช่นนั้น เพราะเราไม่อยากให้คุณต้องรู้สึกเสี่ยงอันตรายจากการติดตั้งแอปของเราเช่นกัน (เพราะคุณก็ต้องโหลด APK ของแอปนี้ไปติดตั้งด้วยตัวเองเช่นกัน) ดังนั้นการทำงานของแอปนี้จึงเป็นแบบออฟไลน์และรบกวนผู้ใช้ให้น้อยที่สุดเท่าที่จะทำได้

## การติดตั้ง
ดาวน์โหลดแอปและติดตั้งผ่านไฟล์ APK ในแต่ละเวอร์ชันได้จากหน้า [Release บน GitHub ของ Repository นี้](https://github.com/akexorcist/ruam-mij-android/releases)

แน่นอนว่าวิธีในการติดตั้งแอปแบบนี้จะไม่ต่างอะไรกับการโหลดไฟล์ APK ของแอปอื่นมาติดตั้งด้วยตัวเอง ซึ่งเป็นหนึ่งในช่องทางสำหรับผู้ที่ไม่ประสงค์ดีและหวังจะใช้ประโยชน์จากการหลอกให้ติดตั้งแอปที่ไม่ปลอดภัยด้วยวิธีแบบนี้

## ถ้ามีคำถามหรือข้อสงสัย
* สามารถตั้งคำถามได้ผ่านหน้า [Issue บน GitHub ของ Repository นี้](https://github.com/akexorcist/ruam-mij-android/issues)

## ผู้ที่มีส่วนรวมในการพัฒนาแอปนี้
* 9arm
* Somkiat Khitwongwattana
* Sorakrich Oanmanee
* เอกลักษณ์ ต่อติด
* Kritsadin Rayanakorn

## ฟีเจอร์ที่ยังไม่ได้ทำ (สำหรับผู้ที่สนใจเข้ามาร่วมพัฒนาด้วย)
* เพิ่มเมนู FAQ ในหน้า About App
* เพิ่มเมนู Open Source License ในหน้า About App
* ทำ Mapping สำหรับ Installer Package Name ให้สะดวกต่อการเข้ามาเพิ่มข้อมูลในภายหลัง
* Cache apps result เก็บไว้ใน Memory จะได้ไม่ต้องสแกนใหม่ทุกครั้งที่เปลี่ยนหน้าไปมา
* เก็บประวัติแอปที่เรียกใช้งาน Media Projection เพื่อให้ผู้ใช้ดูย้อนหลังได้
* ทำ Snapshot Testing
* ทำ CI/CD ด้วย GitHub Actions เพื่อ Publish App ผ่านหน้า Releases โดยอัตโนมัติ

## คำแนะนำสำหรับการ build debug apk จาก source code โดยตรง (สำหรับทดสอบ app แบบ nightly กรณีทีมงานอัพเดท source code ล่าสุดแต่ยังไม่ปล่อย release )
ตรวจสอบให้แน่ใจว่าตั้งค่า environment variable `ANDROID_HOME` ให้ชี้ไปยัง Android SDK ที่ถูกต้อง
และควรตั้งค่า `JAVA_HOME` ให้ชี้ไปยัง JDK ที่ต้องการใช้งานด้วย

```bash
echo $ANDROID_HOME
echo $JAVA_HOME
```
หลังจาก run command ข้างต้น หากเห็น path ชี้ไปยัง SDK และ JDK ที่ต้องการแล้ว ให้ run command ด้านล่างต่อไปนี้เพื่อ build debug apk สำหรับทดสอบ

```bash
git clone https://github.com/akexorcist/ruam-mij-android.git
cd ruam-mij-android

# List all task from gradlew
./gradlew task

# Build a debug apk
./gradlew assembleDebug
```

## License
ดูได้ที่ [LICENSE](LICENSE)

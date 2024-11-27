# flutter-dev
learning flutter development (mobile application)
# Flutter Setup and Testing on macOS

![Flutter Logo](https://flutter.dev/images/flutter-logo-sharing.png)

## 📋 ข้อกำหนดของระบบ
ก่อนเริ่มต้น ให้ตรวจสอบว่า macOS ของคุณมีคุณสมบัติตรงตามข้อกำหนด:
- macOS เวอร์ชัน **10.14** หรือใหม่กว่า
- พื้นที่ว่างอย่างน้อย **2.8 GB**
- ติดตั้ง **Xcode** สำหรับการพัฒนา iOS

---

## 🚀 ขั้นตอนการติดตั้ง Flutter บน macOS

### 1. ดาวน์โหลด Flutter SDK
1. ไปที่เว็บไซต์ [Flutter SDK Downloads](https://flutter.dev/docs/get-started/install/macos)
2. คลิกปุ่ม **macOS** เพื่อดาวน์โหลดไฟล์ `.zip`
3. แตกไฟล์ `.zip` และย้ายโฟลเดอร์ `flutter` ไปยังตำแหน่งที่คุณต้องการ เช่น:
   ```plaintext
   /Users/your_username/development/
   ```

![Download Flutter](https://flutter.dev/assets/images/shared/brand/flutter/logo/flutter-lockup.png)

---

### 2. เพิ่ม Flutter ลงใน PATH
1. เปิด Terminal และแก้ไขไฟล์ `~/.zshrc` (หรือ `~/.bash_profile` หากใช้ Bash):
   ```bash
   nano ~/.zshrc
   ```
2. เพิ่มบรรทัดนี้ลงไป:
   ```bash
   export PATH="$PATH:/Users/your_username/development/flutter/bin"
   ```
3. บันทึกไฟล์และโหลดการตั้งค่าใหม่:
   ```bash
   source ~/.zshrc
   ```

---

### 3. ทดสอบการติดตั้ง
1. เปิด Terminal แล้วพิมพ์คำสั่ง:
   ```bash
   flutter doctor
   ```
2. ตรวจสอบผลลัพธ์ หากมีปัญหาใด ๆ จะมีคำแนะนำให้แก้ไข

![Flutter Doctor Output](https://flutter.dev/assets/images/docs/cli/flutter-doctor.png)

---

## 🛠 ติดตั้งเครื่องมือเพิ่มเติม

### สำหรับ iOS
1. ติดตั้ง **Xcode** จาก App Store
2. เปิด Xcode และไปที่ **Preferences > Locations**
   - ตั้งค่า **Command Line Tools** ให้เป็นเวอร์ชันปัจจุบันของ Xcode

3. ติดตั้ง CocoaPods:
   ```bash
   sudo gem install cocoapods
   ```

---

### สำหรับ Android
1. ดาวน์โหลดและติดตั้ง [Android Studio](https://developer.android.com/studio)
2. เปิด Android Studio และติดตั้ง:
   - **Android SDK**
   - **Command-line Tools**
   - **Android Virtual Device (AVD)**

3. ติดตั้ง Flutter และ Dart Plugins:
   - ไปที่ **Preferences > Plugins**
   - ค้นหา **Flutter** และติดตั้ง (Dart จะติดตั้งโดยอัตโนมัติ)

4. ยอมรับใบอนุญาต Android SDK:
   ```bash
   flutter doctor --android-licenses
   ```

---

## 🎉 ทดสอบ Flutter ด้วยโปรเจกต์แรก

### 1. สร้างโปรเจกต์ใหม่
1. เปิด Terminal แล้วรันคำสั่ง:
   ```bash
   flutter create my_first_app
   cd my_first_app
   ```

### 2. รันแอปบน iOS Simulator
1. เปิด **Simulator** ด้วยคำสั่ง:
   ```bash
   open -a Simulator
   ```
2. รันแอปด้วยคำสั่ง:
   ```bash
   flutter run
   ```

### 3. รันแอปบน Android Emulator
1. เปิด **Android Emulator** ผ่าน Android Studio
2. รันคำสั่งใน Terminal:
   ```bash
   flutter run
   ```

---

## 💡 การแก้ปัญหาเบื้องต้น
- หาก `flutter doctor` แจ้งข้อผิดพลาด:
  - ตรวจสอบว่า Xcode และ Android Studio ติดตั้งครบถ้วน
  - ยืนยันว่า Flutter SDK อยู่ใน PATH โดยพิมพ์ `echo $PATH`
- หาก Emulator ไม่ทำงาน:
  - รีสตาร์ท Android Studio หรือ Xcode
  - อัปเดต SDK และเครื่องมือทั้งหมด

---

## 📚 แหล่งข้อมูลเพิ่มเติม
- [Flutter Official Documentation](https://flutter.dev/docs)
- [DartPad Online Tool](https://dartpad.dev/)
- [macOS Installation Guide](https://flutter.dev/docs/get-started/install/macos)

---

**พร้อมใช้งาน Flutter แล้ว!** 🚀 ลองสร้างแอปแรกของคุณและเริ่มต้นพัฒนาได้เลย!


**Unlock native `SAVE_RESOURCE_FILE` — เขียนไฟล์ใน resource ได้แบบไม่จำกัด**
---
## 📦 ดาวน์โหลด
👉 [**คลิกที่นี่เพื่อดาวน์โหลด**](https://github.com/b3sty191/b3sty_savefileplus/releases)

## 🔧 วิธีติดตั้ง
1. ดาวน์โหลดไฟล์ `scripting-server.dll` จากหน้า **Releases** ใน GitHub ของโปรเจกต์นี้  
2. วางไฟล์ `scripting-server.dll` ลงในโฟลเดอร์ `server/` ของ FiveM แล้ว **ลงทับไฟล์เดิม**
3. ใช้ได้เฉพาะ **Artifact Version 12078 ขึ้นไป**
4. จากนั้น **restart server**  
5. เสร็จสิ้น — สามารถเรียกใช้งาน native `SAVE_RESOURCE_FILE` ได้ทันทีโดยไม่มีการจำกัด

---

## 💡 วิธีใช้งาน
วางโค้ดนี้ในไฟล์ Lua ของ resource ที่ต้องการ (เช่น `server.lua`):

```lua
local success = Citizen.InvokeNative(0xFADEB3B5E56AFE01, 'resource', 'file.txt', "message", -1)

if success then
    print('File saved successfully!')
else
    print('Failed to save file')
end

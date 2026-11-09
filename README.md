# TITAN PRO v2.1.2 — Web (Render)

نسخه وب TITAN PRO GLASS-AUTOPILOT برای استقرار رایگان روی **Render.com**.

## استقرار در ۳ دقیقه

1. فایل `TITAN_PRO_v212_Render.zip` را در **ریشه همین مخزن** آپلود کن و Extract کن (محتوای پوشه `titan_render` باید در ریشه باشد: `app/`, `run.py`, `requirements.txt`, ...)
2. برو به [dashboard.render.com](https://dashboard.render.com) → **New +** → **Web Service**
3. همین مخزن را انتخاب کن
4. تنظیمات:
   - **Name**: `titan-pro` (یا هر اسمی)
   - **Runtime**: Python 3
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `python run.py`
   - **Instance Type**: **Free**
5. Environment:
   - `TITAN_HOST` = `0.0.0.0`
6. **Create Web Service**

بعد از ۱ تا ۳ دقیقه لینک عمومی آماده است.

## محدودیت پلن رایگان

- بعد از ~۱۵ دقیقه بی‌کاری سرویس می‌خوابد (اولین باز شدن بعدی کمی طول می‌کشد)
- دیسک پایدار ندارد → داده‌های پوشه `YYY` با redeploy پاک می‌شوند

## فایل‌های مهم

- `render.yaml` — تنظیمات پیشنهادی Render
- `runtime.txt` — Python 3.11
- `requirements.txt` — وابستگی‌ها
- `run.py` — نقطه شروع

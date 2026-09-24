# VODKA Panel

## ورود اولیه
- رمز پیش‌فرض مرحله اول: `admin`
- بعد از تأیید `admin`، در مرحله دوم یک رمز اصلی جدید با حداقل ۸ کاراکتر تعیین کنید.
- از آن به بعد ورود به پنل با همان **رمز اصلی** انجام می‌شود.

## آدرس پنل
`https://YOUR-WORKER.workers.dev/vodkapanel`

## Cloudflare KV
در Wrangler این Binding را بسازید:
- Binding: `VODKA_KV`
- Namespace ID: شناسه KV خودتان

## Deploy
```bash
npx wrangler deploy
```

> اگر قبلاً رمز اصلی در KV ذخیره شده باشد، مرحله `admin` دوباره نمایش داده نمی‌شود؛ برای شروع مجدد باید مقدار `vodka_master_key_v2` در KV پاک شود.


## VODKA Admin
- Panel entry: `/vodkapanel`
- Default admin password: `admin`
- The login backend accepts `admin` as the fixed VODKA admin key.
- Keep `VODKA_KV` bound in Cloudflare for persistent settings/users.

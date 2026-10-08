# VALER × Salla — Electronic Invoice Template

قالب فاتورة إلكترونية/ضريبية بتصميم VALER، مخصص للعرض والطباعة والحفظ بصيغة PDF داخل متجر Salla أو أي طبقة تكامل تستقبل بيانات الطلب.

## الملفات

- `invoice/valer-invoice.html` — قالب A4 متجاوب وقابل للطباعة.
- `invoice/invoice-data.example.json` — مثال واضح لهيكل بيانات الفاتورة.

## تمرير بيانات الطلب

قبل تحميل القالب يمكن تمرير بيانات الطلب من Salla أو طبقة التكامل بهذا الشكل:

```js
window.VALER_INVOICE_DATA = {
  invoiceNumber: "INV-2026-000001",
  orderNumber: "ORD-2026-000001",
  issueDate: "2026-10-08T00:00:00+03:00",
  customerName: "اسم العميل",
  shippingAddress: "عنوان الشحن",
  customerPhone: "+966500000000",
  customerEmail: "customer@example.com",
  customerVatNumber: "",
  discount: 0,
  shippingFee: 0,
  vatRate: 0.15,
  invoiceType: "simplified",
  seller: {
    nameAr: "ڤالير للأقمشة",
    nameEn: "VALER Luxury Fabrics",
    vatNumber: "ضع الرقم الرسمي هنا",
    commercialRegistration: "ضع الرقم الرسمي هنا",
    phone: "+966500000000",
    email: "Valer.ufco@gmail.com",
    address: "الرياض، المملكة العربية السعودية"
  },
  products: []
};
```

## مهم بخصوص ZATCA

هذا المشروع **قالب عرض وطباعة** وليس نظام فوترة إلكترونية كاملًا. لا يدّعي القالب بمفرده التسجيل أو التوقيع أو الإرسال أو التخليص لدى هيئة الزكاة والضريبة والجمارك (ZATCA).

يمكن للقالب إنشاء QR بصيغة TLV لعرض بيانات الفاتورة، لكن **الـQR الرسمي ومتطلبات المرحلة الثانية والتوقيع والتشفير والربط مع ZATCA يجب أن تأتي من نظام الفوترة أو التكامل المعتمد المستخدم فعليًا في المتجر**.

لا تضع رقم VAT أو السجل التجاري التجريبي الموجود في ملفات المثال على فواتير حقيقية؛ استبدلهما بالبيانات الرسمية للمنشأة.

## التشغيل

للتطوير:

```bash
pnpm install
pnpm run dev
```

ولبناء ملفات الإنتاج:

```bash
pnpm run build
```

## Repository

`https://github.com/intteeam-gif/tw-mgmoaah-valer`

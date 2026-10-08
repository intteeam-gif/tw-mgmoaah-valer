# VALER × Salla — Electronic Invoice Template

قالب فاتورة إلكترونية/ضريبية بتصميم VALER، جاهز للدمج داخل مشروع متجر Salla.

### الملفات
- `invoice/valer-invoice.html` — قالب A4 قابل للطباعة والحفظ PDF.
- `invoice/invoice-data.example.json` — مثال لهيكل بيانات الطلب.

### نقطة الربط
يتم تمرير بيانات الطلب إلى القالب عبر:
```js
window.VALER_INVOICE_DATA = {
  invoiceNumber, orderNumber, customerName,
  discount, shippingFee, vatRate, products, seller
};
```

### تنبيه مهم
القالب مسؤول عن **العرض والطباعة**. لا يعتبر بحد ذاته نظام فوترة ZATCA Phase 2 ولا يقوم بالتوقيع أو الإرسال/التخليص لدى ZATCA. يجب أن تأتي بيانات الفاتورة الرسمية والـQR الرسمي من نظام الفوترة/التكامل المعتمد.

تم فصل بيانات الطلب عن التصميم حتى يمكن ربطه بطبقة Salla/API دون إعادة بناء الواجهة.

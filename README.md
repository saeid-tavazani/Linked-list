مطمئناً، اینجا یک فایل README.md به زبان فارسی برای کلاس `LinkedList` شما آمده است:


# پیاده‌سازی لیست پیوندی در جاوااسکریپت

این یک پیاده‌سازی ساده از یک لیست پیوندی تکی در جاوااسکریپت است. لیست پیوندی یک ساختار داده خطی است که در آن عناصر در گره‌ها ذخیره می‌شوند. هر گره به گره بعدی در توالی اشاره می‌کند.

## استفاده

ابتدا یک نمونه جدید از `LinkedList` ایجاد کنید:

```javascript
const list = new LinkedList();
```

### `append(value)`

یک گره جدید با مقدار داده شده `value` به انتهای لیست اضافه می‌کند.

```javascript
list.append(5);
list.append(10);
list.append(15);
```

نتیجه لیست پیوندی:
```
5 -> 10 -> 15
```

### `prepend(value)`

یک گره جدید با مقدار داده شده `value` به ابتدای لیست اضافه می‌کند.

```javascript
list.prepend(2);
list.prepend(1);
```

نتیجه لیست پیوندی:
```
1 -> 2 -> 5 -> 10 -> 15
```

### `insertAfter(value, afterValue)`

یک گره جدید با مقدار داده شده `value` بعد از گره با مقدار `afterValue` وارد می‌کند.

```javascript
list.insertAfter(8, 5);
```

نتیجه لیست پیوندی:
```
1 -> 2 -> 5 -> 8 -> 10 -> 15
```

### `find(value)`

اولین گره با مقدار داده شده `value` را پیدا کرده و برمی‌گرداند.

```javascript
const node = list.find(10);
console.log(node.value); // خروجی: 10
```

### `delete(value)`

تمام گره‌ها با مقدار داده شده `value` را از لیست حذف می‌کند.

```javascript
list.delete(5);
```

نتیجه لیست پیوندی:
```
1 -> 2 -> 8 -> 10 -> 15
```

### `toArray()`

لیست پیوندی را به یک آرایه از گره‌ها تبدیل می‌کند.

```javascript
const arr = list.toArray();
console.log(arr.map(node => node.value)); // خروجی: [1, 2, 8, 10, 15]
```

## مثال

```javascript
const list = new LinkedList();

list.append(5);
list.append(10);
list.prepend(2);
list.insertAfter(8, 5);
list.delete(5);

console.log(list.toArray().map(node => node.value)); // خروجی: [2, 8, 10]
```

## نکات

- اگر `value` در لیست وجود نداشته باشد برای متدهای `find` یا `delete`، این متدها بدون ایجاد تغییرات بازمی‌گردند یا عملیات می‌کنند.


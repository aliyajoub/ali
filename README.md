# نظام الأمن والمراقبة الذكي | Smart Security and Surveillance System

## نظرة عامة | Overview

**العربية:**

نظام الأمن والمراقبة الذكي هو حل متكامل للمراقبة الأمنية يستخدم تقنيات الذكاء الاصطناعي المتقدمة للكشف عن الأسلحة والتعرف على الوجوه في الوقت الفعلي. يعتمد النظام على نماذج YOLO (You Only Look Once) للكشف عن الأجسام وتحديد الأسلحة المحتملة مثل المسدسات والسكاكين والبنادق، مع إمكانية التعرف على الأشخاص المصرح لهم وغير المصرح لهم.  

يوفر النظام آلية تنبيه فورية عند اكتشاف تهديدات محتملة، مع تسجيل الصور وحفظها للرجوع إليها لاحقًا. تم تصميم النظام ليكون خفيفًا وفعالًا، مع إمكانية تشغيله على أجهزة ذات موارد محدودة.

**English:**

The Smart Security and Surveillance System is an integrated security monitoring solution that utilizes advanced artificial intelligence techniques to detect weapons and recognize faces in real-time. The system relies on YOLO (You Only Look Once) models for object detection and identification of potential weapons such as guns, knives, and rifles, with the ability to recognize authorized and unauthorized individuals.

The system provides an immediate alert mechanism when potential threats are detected, with image recording and storage for later reference. The system is designed to be lightweight and efficient, with the ability to run on devices with limited resources.

## المميزات الرئيسية | Key Features

**العربية:**

- **الكشف عن الأسلحة**: استخدام نماذج YOLO للكشف عن مجموعة واسعة من الأسلحة بدقة عالية
- **التعرف على الوجوه**: تحديد الأشخاص المصرح لهم وغير المصرح لهم (قيد التطوير)
- **تنبيهات فورية**: إطلاق إنذارات عند اكتشاف تهديدات محتملة
- **تسجيل الأحداث**: حفظ الصور والإطارات المهمة للتحليل اللاحق
- **واجهة تحكم بسيطة**: سهولة التشغيل والإيقاف والتحكم في النظام
- **أداء محسّن**: تقنيات لتقليل استهلاك الموارد وتحسين الأداء على الأجهزة المختلفة
- **تخزين الإطارات**: حفظ الإطارات المعالجة في مجلد مخصص للمراجعة اللاحقة

**English:**

- **Weapon Detection**: Using YOLO models to detect a wide range of weapons with high accuracy
- **Face Recognition**: Identifying authorized and unauthorized individuals (under development)
- **Instant Alerts**: Triggering alarms when potential threats are detected
- **Event Recording**: Saving images and important frames for later analysis
- **Simple Control Interface**: Easy operation, stopping, and system control
- **Optimized Performance**: Techniques to reduce resource consumption and improve performance on different devices
- **Frame Storage**: Saving processed frames in a dedicated folder for later review

## المتطلبات | Requirements

**العربية:**

1. Python 3.7 أو أحدث
2. كاميرا ويب متصلة
3. مكتبات Python المطلوبة (OpenCV, NumPy, Ultralytics YOLO)
4. وحدة معالجة مركزية قوية (يُفضل وجود وحدة معالجة رسومات لأداء أفضل)

**English:**

1. Python 3.7 or newer
2. Connected webcam
3. Required Python libraries (OpenCV, NumPy, Ultralytics YOLO)
4. Powerful CPU (GPU recommended for better performance)

## التثبيت | Installation

**العربية:**

1. قم بتثبيت المتطلبات:
```bash
pip install -r requirements.txt
```

2. قم بتحميل نموذج YOLO المطلوب:
   - النظام يستخدم نموذج `yolov8n.pt` افتراضيًا (سيتم تحميله تلقائيًا عند أول تشغيل)
   - يمكنك استخدام نماذج أخرى من YOLO بتعديل المسار في ملف `security_system.py`

**English:**

1. Install the requirements:
```bash
pip install -r requirements.txt
```

2. Download the required YOLO model:
   - The system uses the `yolov8n.pt` model by default (will be downloaded automatically on first run)
   - You can use other YOLO models by modifying the path in the `security_system.py` file

## الإعداد | Configuration

**العربية:**

يمكن تعديل إعدادات النظام في ملف `security_system.py`:

- `alert_cooldown`: الوقت بين التنبيهات (بالثواني)
- `frame_save_interval`: عدد الإطارات بين كل عملية حفظ
- `output_dir`: مجلد حفظ الإطارات المعالجة
- قائمة `weapon_types`: أنواع الأسلحة التي يتم البحث عنها
- `weapon_class_ids`: معرفات فئات الأسلحة في مجموعة بيانات COCO

**English:**

System settings can be modified in the `security_system.py` file:

- `alert_cooldown`: Time between alerts (in seconds)
- `frame_save_interval`: Number of frames between each save operation
- `output_dir`: Folder for saving processed frames
- `weapon_types` list: Types of weapons to search for
- `weapon_class_ids`: Weapon class IDs in the COCO dataset

## تشغيل النظام | Running the System

**العربية:**

1. قم بتشغيل الملف الرئيسي:
```bash
python run.py
```

2. استخدم واجهة التحكم البسيطة للتحكم في النظام
3. اضغط على 'q' للخروج من النظام

**English:**

1. Run the main file:
```bash
python run.py
```

2. Use the simple control interface to control the system
3. Press 'q' to exit the system

## تطوير النظام | System Development

**العربية:**

النظام قابل للتوسعة ويمكن إضافة المزيد من الميزات إليه مثل:

- تحسين دقة الكشف عن الأسلحة
- تطوير نظام التعرف على الوجوه
- إضافة آليات تنبيه إضافية (مثل الرسائل النصية أو البريد الإلكتروني)
- دعم تعدد الكاميرات
- تطوير واجهة مستخدم رسومية متقدمة

**English:**

The system is expandable and more features can be added to it such as:

- Improving weapon detection accuracy
- Developing the face recognition system
- Adding additional alert mechanisms (such as SMS or email)
- Supporting multiple cameras
- Developing an advanced graphical user interface

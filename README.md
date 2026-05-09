D3 is an new update version of index 

✅ التعديلات التي تم تنفيذها
1️⃣ ترتيب الأيام في Edit Plan (تحريك لأعلى/لأسفل)
أضفت في نافذة Edit Plan بجانب كل يوم زرين: ↑ و ↓.

الضغط على ↑ ينقل اليوم لأعلى (يبدل ترتيبه مع اليوم الذي قبله).

الضغط على ↓ ينقل اليوم لأسفل (يبدل ترتيبه مع اليوم الذي بعده).

عند التبديل، يتم تحديث ترتيب editorPlan.days وكذلك editorPlan.exercisesByDay و editorPlan.daySpecificCrossFit بشكل متزامن.

2️⃣ جعل خانات Sets غير قابلة للتعديل
في دالة renderTable، قمت بتغيير خلية Sets من <input> إلى <span> يعرض قيمة data.sets كنص عادي.

المستخدم لم يعد يستطيع تعديل عدد المجموعات يدوياً. القيمة تؤخذ من week.plan.exerciseSets أو من defaultSetsMap.

3️⃣ إعادة ترقيم الأسابيع تلقائياً عند الحذف أو الإضافة
أضفت دالة جديدة renumberWeeks():

تعيد تعيين weekNumber لكل أسبوع في allWeeks حسب ترتيبه (1, 2, 3, ...).

تحديث weekSelect وعرض الأرقام الصحيحة.

يتم استدعاء هذه الدالة بعد:

deleteCurrentWeek

addNewWeek

cloneCurrentWeek

importJson

resetAllData (لأنها تعيد بناء الأسابيع)

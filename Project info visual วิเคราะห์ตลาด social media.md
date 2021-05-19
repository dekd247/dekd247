title:การวิเคราะห์ตลาด Platform Social media

desc:เป้าหมายของ Project นี้คือการสำรวจว่า Platform ไหนมีผู้ใช้เยอะสุด การเปลี่ยนแปลงของ Engagement ในแต่ละเดือนของแต่ละ Platform กลุ่ม Influencer ในแต่ละ Platform และ Platform นั้นคนพูดถึงเรื่องอะไรบ้างโดยการตลาดบน Social Media ในปัจจุบันจำเป็นจะต้องใช้ข้อมูลเหล่านี้เพื่อประกอบการตัดสินใจในการลงทุนใน Platform นั้นๆ

thumbnail:

![visualization (2)](https://user-images.githubusercontent.com/83722061/117236122-4bf79480-ae52-11eb-9b88-7ee53474a3f1.png)

proj-url:https://prezi.com/i/yf93oxrxvqzc/

viz: [Bar Chart, Line Chart,Pie Chart,Scatter Plot,Wordcloud]

tools: [Altair,Python,PowerBI,Excel,Prezi]

## ข้อมูล
ใช้ Dataset ของคุณต่อใน Google Classroom
## Valdiate
**Platform ไหนคนใช้เยอะสุด**
ผมจะพิสูจน์ว่า platform ไหนเยอะสุด โดยผมจะสร้างกราฟ pie chart  ออกเป็น 4 กราฟได้แก่ 

1.Engagement ที่รวม like dislike share retweet ของแต่ละ platform 
2.Engagement + View จะรวมยอด view ไปด้วยซึ่งยอด View จะมี 2 Platform คือ IG และ Youtube 
3.ยอด Fan ที่จะรวมยอดผู้ติดตามต่างๆ ในแต่ละ Platform 
4.จำนวน User ที่จะรวบรวม จำนวน User Influencer ในแต่ละ Platform

ซึ่งในการวัดว่า Platform ไหนผู้ใช้เยอะสุดเราได้วัดจากการทำ Quality Metric โดยถ้า Platform ไหนมีจำนวน % เยอะสุดใน pie chart หัวข้อนั้นๆ จะได้ 4 คะแนน ส่วนลำดับรองลงมาก็จะได้คะแนน 3 2 และ 1 ตามลำดับ ทำแบบนี้ทั้งหมด 4 กราฟแล้วรวมคะแนน
โดย Platform ที่มีคะแนนมากสุดก็จะหมายความว่ามีคนใช้เยอะสุดในปี 2020

**การดูว่า Influencer หรือ User กลุ่มไหนครอบครอง แต่ละ Platform**

ก่อนอื่นต้องแยก user ออกมาก่อนโดยที่ผมจะทำการแยก User ที่มี Engagement รวมกันประมาณ 50 %แรก ของทั้ง Platform ทำแบบนี้ 4 Platform หลังจากนั้นก็ทำการสำรวจว่า User นี้ทำ Content เกี่ยวกับอะไรหลังจากนั้นก็ทำการจับกลุ่มกันในแต่ละ Platform

หลังจากที่แยก User แต่ละ Platform เสร็จแล้ว ผมจะทำการแบ่งกราฟออกมาเป็น 5 กราฟ ซึ่งแต่ละกราฟจะแสดงถึงว่า influencer กลุ่มไหนครอบครองด้านอะไรบ้างในแต่ละ Platform โดยกราฟ5กราฟ จะมี
1. scatter plot ที่แกน X เป็นยอด Fan และ y เป็นยอด Engagement สามารถมองได้ว่า User ไหน อยู่ลำดับไหนบนแต่ละ Platform (เหมาะสำหรับดูว่า User แบบรายเดี่ยว)
2. Pie Chart Engagement กราฟนี้จะสามารถบอกได้ว่า  influencer กลุ่มไหนครอบครอง engagement 50% แรก มากสุดบนแต่ละ Platform เปรียบได้ว่าเป็นกลุ่มที่มีอิทธิพลด้าน Engagement บน Platform นั้น
3. Pie Chart Fan/Subscribe กราฟนี้จะบอกว่า ในกลุ่ม influencer กลุ่มไหนมียอดแฟนเยอะสุด  เปรียบได้ว่าเป็นกลุ่มที่มีอิทธิพลด้าน Fan บน Platform นั้นๆ
4. Pie Chart Point-eng จะบอกเป็นแบบราย user กล่าวคือถ้าเราเป็น influencer นี้ จะมีโอกาสได้ engagement เยอะสุดหรือไม่ คำนวนโดย (Point-Eng = engagement ของกลุ่ม influencer/จำนวน influencer ของกลุ่ม)
5. Pie Chart Point-fan จะบอกเป็นแบบราย user กล่าวคือถ้าเราเป็น influencer นี้ จะมีโอกาสได้ fan เยอะสุดหรือไม่ (Point-Fan = Fan ของกลุ่ม influencer/จำนวน influencer ของกลุ่ม)

กราฟ 2-5 จะวัดจาก % มากสุด กล่าวคือถ้า กลุ่ม Influencer กลุ่มไหนมี % มากสุดก็หมายความว่าก็เป็นลำดับ 1 ในด้านนั้นๆ
มีกราฟ engagement แล้วทำไมต้องทำ point-eng อีก เนื่องจากอาจจะมีกรณีที่ influencer ประเภทนั้นมีจำนวนเยอะมากส่งผลให้มียอด engagement รวมเยอะ แต่ แต่ละ user มี engagement น้อยมาก ดังนั้น point-engจึงเหมือนเป็นเครื่องมือช่วยดูว่า influencer แต่ละประเภทมียอด engagement ที่แท้จริงมีเท่าไหร่
อย่างไรก็ตาม point-eng จะด้อยประสิทธิภาพ เมื่อจำนวน influencer ในประเภทนั้นๆ มีน้อยกว่า 5
โดยข้อ 2 - 5 หากกลุ่ม Influencer ไหนมีจำนวน % ใน Pie Chart เยอะสุดก็จะครอบครองในด้านนั้นๆ
*หมายเหตุ Engagement ใน Platform Youtube จะวัดจาก Engagement + View เพราะ Platform Youtube จะวัดความ Popular จะวัดจากยอด View

**การพิสูจน์ว่าแต่ละ Platform พูดถึงเรื่องอะไรมากสุดในปี 2020**

ผมจะทำการแบ่งออกมาเป็น 2 visualisation เพื่อเป็น visual evidence ในการพิสูจน์โดยประกอบไปด้วย
1. Wordcloud Wordcloud เป็นอีก 1 เครื่องมือที่ช่วยดูว่าทั้ง Platform กำลังพูดถึงเรื่องอะไร โดย เราจะสังเกตจากศัพท์ที่มีตัวใหญ่หรือกลุ่มคำศัพท์ที่คล้ายกัน ก็จะสามารถบอกได้แล้วว่า Platform นี้พูดถึงเรื่องอะไรเช่น Twitter คำศัพท์ที่ใช้กันเยอะก็จะมี 14ตุลา ปลดแอค ซึ่ง
คำศัพท์เหล่านี้เป็นศัพท์เกี่ยวกับการเมืองก็หมายความว่า Platform Twitter พูดเกี่ยวกับการเมือง อย่างไรก็ตามต้องมีการกรองข้อความจากการ Spam ด้วยเนื่องจากจะทำให้ผลลัพธ์ Wordcloud คลาดเคลื่อนได้
โดยเราได้ทำการ filter ข้อความเนื่องจากการ Spam ด้วยการตั้งเกณฑ์ดังนี้
* Wordcloud Platform Youtube คัดมาเฉพาะข้อความ ที่มียอด View > 20000 
* Wordcloud Platform Facebook คัดมาเฉพาะข้อความ ที่มียอด Engagement > 5000 
* Wordcloud Twitter คัดมาเฉพาะที่ ข้อความ Engagement > 2500
* Wordcloud IG คัดมาเฉพาะที่ ข้อความ Engagement > 2500


2. Line Chart เวลา
Line Chart เวลา ที่แกน x จะเป็นเดือน และแกน y จะเป็น Percent การเปลี่ยนแปลงของ Engagement โดยที่ตั้งเดือนมกราคมเป็นเดือนฐาน กราฟนี้จะสามารถพิสูจน์ได้ว่าการเปลี่ยนแปลง Engagement ของแต่ละ Platform เกี่ยวข้องกับเหตุการณ์บ้านเมืองหรือไม่ เช่นเดือนตุลาที่มีเหตุการณ์การประท้วงอย่างหนัก
โดย Platform Facebook และ Twitter มียอด engagement พุ่งขึ้นอย่างเห็นได้ชัด แก็สามารถบอกได้ว่า Platform Twitter หรือ Facebook อาจจะเกี่ยวกับการเมือง หรือข่าวสาร หาก Platform ไหนมีเส้นไม่เปลี่ยนแปลงตามเหตุการณ์บ้านเมืองก็จะสรุปได้ว่าไม่สามารถบอกได้ว่า Platform นั้นพูดถึงเรื่องอะไรด้วยการใช้ Pie Chart นอกจากนี้ Line Chart นี้สามารถพิสูจน์ได้ว่าภาพของ Engagement ในแต่ละ Platform เป็นอย่างไร
เช่นถ้าเส้น youtube มีทิศทางลงก็หมายความว่าคนไม่ค่อยใช้งาน Youtube ในช่วงปี 2020 

อย่างไรก็ตาม การพิสูจน์ว่าแต่ละ Platform พูดถึงเรื่องอะไรมากสุดในปี 2020 อาจจะต้องใช้ข้อมูลกลุ่ม Influencer ประกอบด้วยเนื่องจากข้อความบาง Platform อาจจะมีการ Spam โดยเฉเพาะข้อความการขายของ แม้ว่ากรองด้วยยอด Engagement แล้ว หรือ Line Chart ไม่สามารถบอกอะไรได้
## สรุป
![Capture](https://user-images.githubusercontent.com/83722061/117255798-46ab4180-ae74-11eb-885e-90f83be0fde4.PNG)




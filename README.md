title:การวิเคราะห์ตลาด Platform Social media

desc:เป้าหมายของ Project นี้คือการสำรวจว่า Platform ไหนมีผู้ใช้เยอะสุด การเปลี่ยนแปลงของ Engagement ในแต่ละเดือนของแต่ละ Platform กลุ่ม Influencer ในแต่ละ Platform และ Platform นั้นคนพูดถึงเรื่องอะไรบ้างโดยการตลาดบน Social Media ในปัจจุบันจำเป็นจะต้องใช้ข้อมูลเหล่านี้เพื่อประกอบการตัดสินใจในการลงทุนใน Platform นั้นๆ

viz: [Bar Chart, Line Chart,Pie Chart,Scatter Plot,Wordcloud]

tools: [Altair,Python,PowerBI,Excel,Prezi]

thumbnail:

![visualization (2)](https://user-images.githubusercontent.com/83722061/117236122-4bf79480-ae52-11eb-9b88-7ee53474a3f1.png)
## ข้อมูล
ใช้ Dataset ของคุณต่อใน Google Classroom
## validation
ลำดับแรกต้องวิเคราะห์ก่อนว่า Platform ไหนมีผู้ใช้เยอะสุดนการดู Platform ไหนใช้เยอะสุด เราจะแบ่งกราฟออกเป็น 4 กราฟได้แก่ 1.Engagement ที่รวม like dislike share retweet ของแต่ละ platform 2.Engagement + View จะรวมยอด view ไปด้วยซึ่งยอด View จะมี 2 Platform คือ IG และ Youtube 3.ยอด Fan ที่จะรวมยอดผู้ติดตามต่างๆ ในแต่ละ Platform 4.จำนวน User ที่จะรวบรวม จำนวน User Influencer ในแต่ละ Platform
ซึ่งในการวัดว่า Platform ไหนผู้ใช้เยอะสุดเราได้วัดจากถ้า Platform ไหนมีจำนวนเยอะสุดในหัวข้อนั้นๆ จะได้ 4 คะแนน ส่วนลำดับรองลงมาก็จะได้คะแนน 3 2 และ 1 ตามลำดับ 
2. ดูเปอร์เซนต์การเปลี่ยนแปลงของ Engagement ในแต่ละเดือนการทำกราฟเวลาสามารถใช้เป็นหลักฐานได้ว่า Platform นี้จะมี User พูดถึงเกี่ยวกับอะไรบ้าง
3.ทำการแยก influence ที่ครอบครอง engagement 50 % แรก ด้วยขบวนการนี้ทำให้เราสามารถแยกได้ว่า influencer คนนี้ทำ content เกี่ยวกับอะไรซึ่งสามารถทำได้ง่ายมากเพราะมีจำนวนน้อย โดยผมสมมุติฐานไว้ว่า influecner เหล่านี้จะเกี่ยวกับการทำ content ของ Platform โดยรวม
เช่นถ้า platform youtube มีการแยก influencer ออกมาแล้วเป็น Gamer เยอะก็จะสรุปได้ว่า Platform Youtuber จะเกี่ยวกับเกมเป็นหลัก หรือถ้า Twitter มี User influencer ที่แยกออกมาแล้วเกี่ยวกับการเมืองเยอะ ก็อาจจะเป็นไปได้ว่าทั้ง Platform Twitter จะเกี่ยวกับ การเมือง
การเมือง โดยการทำ influencer จะต้องประกอบไปด้วยกราฟ 
1. scatter plot ที่แกน X เป็นยอด Fan และ y เป็นยอด Engagement
2. Engagement กราฟนี้จะสามารถบอกได้ว่า Engaggement 50% ของแต่ละ platform influencer กลุ่มไหนครอบครองมากสุด
3. Fan/Subscribe กราฟนี้จะบอกว่า ในกลุ่ม influencer ที่กล่าวมาในข้อ 2 กลุ่มไหนมียอดแฟนเยอะสุด
4. Point-eng จะบอกเป็นแบบราย user กล่าวคือถ้าเราเป็น influencer นี้ จะมีโอกาสได้ engagement เยอะสุดหรือไม่ คำนวนโดย (engagement ของ influencer/จำนวน influencer)
5. Point-fan จะบอกเป็นแบบราย user กล่าวคือถ้าเราเป็น influencer นี้ จะมีโอกาสได้ fan เยอะสุดหรือไม่ (Fan ของ influencer/จำนวน influencer)
6. Wordcloud Wordcloud เป็นอีก 1 เครื่องมือที่ช่วยดูว่าทั้ง Platform กำลังพูดถึงเรื่องอะไร โดย wordcloud สามารถเป็นเครื่องมือในการช่วยตัดสินใจ

ผลลัพธ์ที่ออกมาโดยสามารถดูรายละเอียดเพิ่มเติมได้ที่ URL ข้างบนเนื่องจากบางผลลัพธ์จำเป็นที่จะต้องใช้รูปดูประกอบ
## 1. Platform ที่คนใช้มากสุด
![dekd1](https://user-images.githubusercontent.com/83722061/117239304-bca1af80-ae58-11eb-901b-1a0129df66aa.PNG)

Facebook>Youtube>IG>Twitter
## 2.การทำ line chart 
ในการทำ line chart เกี่ยวกับการใช้งานของแต่ละ Platform ในแต่ละช่วงเวลา เราได้ตั้งเดือนมกราคมเป็นเดือนฐาน เดือนต่อๆ มาจะลบด้วยเดือนฐานและหารด้วยเดือนฐาน คูณ 100ผลลัพธ์ที่ออกมาจะได้เป็น Percentage การเจริญเติบโตของEngagement โดยจะเห็นได้ว่า Twitter และ Facebook จะ
มีแนวโน้มไปในทางเดียวกัน กล่าวคือยอดเปอร์เซนต์จะพุ่งขึ้นเมื่อเกิดเหตุการณ์สำคัญในบ้านเมือง เรายังสามารถตั้งสมมุติฐานไปได้อีกว่า กลุ่ม Influencer น่าจะเกี่ยวกับข่าวสาร หรือไม่ก็ผู้ใช้ platform ที่ชอบการเมืองมากๆ Platform IG คล้ายๆกับ Twitter และ Facebook แต่เส้นจะคงตัวมากกว่า และ Platform
Youtube จะไม่อิงกับ Platform ใดๆเลย ซึ่งในเดือน 2020 เป็นขาลงของ Youtube
## 3.Platform Youtube
ผลลัพธ์จากการแยก influencer พบว่า Youtuberเหนือกว่าในด้าน Engagement ยอด Subscribe และจำนวน User แต่เมื่อเทียบเป็น ราย User พบว่า การทำ content Gamer มีโอกาสได้ยอด Engagement สูงกว่าแต่ยอด subscribe ยังแพ้ Youtuber

***ผลลัพธ์ Wordcloud*** ส่วนใหญ่พูดเกี่ยวกับการลงโฆษณา การกด like Subscribe แล้วคำศัพท์เกี่ยวกับ Game
จึงสรุปได้ว่า Platform Youtube เกี่ยวกับ เกมและ Youtuber ซึ่งสามารถแยกได้อีกว่าเป็น game อะไร หรือ youtube ทำเกี่ยวกับอะไรอ่านรายละอียดเพิ่มเติมได้ที่ URL ข้างบน
## 4.Platform Facebook
ผลลัพธ์จาก Influencer
โดย ประเภทของ influecner มีดังนี้
beauty blocker
youtuber
ครอบครัว
ครีเอเตอร์วิดีโอ
คำคม
ดูดวง
ตลาด
ท่องเที่ยว
บันเทิง
ภาพยนตร์
รถยนต์
สัตว์เลี้ยง
สื่อ
อาหาร จากผลลัพธ์จะเห็นได้ว่า User ประเภทสื่อจะครอบครอง Engagement บน Platform Facebook และ User ที่ทำเกี่ยวกับอาหารจะมียอด Fan หรือคนกด like page เยอะ นอกจากนี้จากการสำรวจพบว่าจำนวน User ที่มากที่สุดบน Platform 
Facebook คือ User ที่ทำเกี่ยวกับสื่อ และ อาหารเมื่อเทียบเป็นราย User หรือ Point พบว่า การทำ User ประเภทสื่อ จะมีโอกาสที่จะได้ยอด Engagement สูงที่สุด ในขณะที่การทำ User ประเภทตลาด จะมียอดคนกดถูกใจเพจสูงที่สุด

***ผลลัพธ์ Wordcloud***
## 5.Platform Twitter 
ผลลัพธ์จาก Influencer
โดย ประเภทของ influecner มีดังนี้
T/ALL  บัญชีทวิตเตอร์ที่โพสเนื้อหาไม่เจาะจง
T/ANIMAL บัญชีทวิตเตอร์ที่โพสเกี่ยวกับสัตว์
T/E  บัญชีทวิตเตอร์ที่โพสเกี่ยวกับความบันเทิง
T/P  บัญชีทวิตเตอร์ที่โพสเกี่ยวกับการเมือง
T/N  บัญชีทวิตเตอร์ช่องข่าว
T/T  บัญชีทวิตเตอร์ที่โพสเกี่ยวกับการเดินทาง
B/B  บัญชีเกี่ยวกับ beauty blocker
R/ALL บัญชีเกี่ยวกับการรีวิวทุกอย่าง
R/J  บัญชีเกี่ยวกับการรีวิวที่เกี่ยวกับ japan
จากการสำรวจข้อมูล engagement ของ twitter พบว่าส่วนใหญ่ของบัญชีที่มียอด engagement เยอะจะเป็นบัญชีที่เกี่ยวกับทุกอย่างโดยมียอด engagement ที่ 35.77% หรือยอดอยู่ที่31178648 รองลงมาจะเป็นบัญชีที่เกี่ยวกับความบันเทิง มียอด engagement 20.18% หรือมียอด engagemant 17587629 
และบัญชีที่เกี่ยวกับสัตว์มียอด engagement 16.35% หรือมียอด engagemant 14424933 แต่ในทางกลับกันยอดfan บัญชีที่มีมากสุดเป็นบัญชีที่เกี่ยวกับความบันเทิง รองลงมาคือบัญชีที่โพสทุกอย่าง แล้วก็เป็น beauty blocker ตามลำดับเมื่อเทียบกับยอด Fan พบว่ากลุ่ม 
Twitter ที่เกี่ยวกับความบันเทิงมียอดผู้ติดตามเยอะสุด นอกจากนี้จำนวน influencer ที่เยอะสุดคือ influecer ที่เป็นชาวทวีตที่โพสทุกอย่างไม่เจาะจงเมื่อเทียบเป็นราย User พบว่า User Twitter ที่โพสเกี่ยวกับสัตว์มีโอกาสที่จะได้ Engagement สูงที่สุด 
ในขณะที่การทำ Twitter เกี่ยวกับ Beauty Blocker มีโอกาสที่จะได้ยอด follow สูงสุดอย่างไรก็ตามการวัดเป็นราย User จะไม่ค่อยแม่นยำเนื่องจาก จำนวน Influence แต่ละประเภทมีน้อยเกินไป๒

***ผลลัพธ์ Wordcloud*** จากการสำรวจ Wordcloud Twitter พบว่าคำที่ใช้ส่วนใหญ่จะเกี่ยวกับการเมืองเช่น หยุดคุกคามประชาชน 16 ตุลาไปแยกปทุมวัน เยาวชนปลดแอก 16 ตุลาไปแยกราชประสงค์ซึ่งจะตรงกับสมมุติฐานจากกราฟเส้นหน้า3 ที่บอกไว้ว่า Platform Twitter 
จะอิงกับข่าวสารบ้านเมืองและในช่วงเดือนตุลาคมกราฟเส้น Platform Twitter จะพุ่งขึ้นมาอย่างมากซึ่งตรงกับ Wordcloud พอดี นอกจากนี้ยังมีศัพท์เกี่ยวกับการขายของเช่น ร้าน แจก บาท  และยังมีศัพท์เกี่ยวกับ Beauty Blocker เช่น ลิป พาเลท สี และยังมีศัพท์เกี่ยวกับเกาหลีเช่น รีวิวเกาหลี Got7 BTS ซึ่งอาจเป็นไปได้ว่า Influencer 
กลุ่มเล็กที่เกี่ยวกับวงเกาหลี อาจจะกระจายกันจนทำให้ไม่มี User ใดที่อยู่ในกลุ่มครอบครอง 50 % engagement แรกอย่างไรก็ตามจาก wordcloud 
จะสรุปได้ว่า Platform Twitter จะเกี่ยวกับการเมืองเป็นหลักเป็นไปได้ว่าที่กลุ่ม T/All หรือ T/E หรือ ทุกกลุ่มจะทวีตเกี่ยวกับการเมืองด้วย
## 6.Platform IG
ผลลัพธ์จาก Influencer
โดย ประเภทของ influecner มีดังนี้
ACTRESS/A บัญชีของนักแสดงหญิง
ACTOR/A บัญชีของนักแสดงชาย
Y/SOLO บัญชีของ youtuber ที่ถ่ายทำคนเดียว
Y/TEAM บัญชีของ youtuber ที่ถ่ายทำเป็นทีม
R/A บัญชีที่รีวิวของทุกอย่าง
R/K บัญชีที่รีวิวเกี่ยวกับเด็ก
E/A บัญชีที่เกี่ยวกับการ entertain
ขายของ/ALL บัญชีที่เน้นการขายของทุกอย่าง
ดูดวง/L บัญชีที่เกี่ยวกับการดูดวง
จากการสำรวจข้อมูล engagement ของ ig พบว่าส่วนใหญ่ของบัญชีที่มียอด engagement เยอะจะเป็นบัญชีที่เกี่ยวกับนักแสดงหญิง มียอด engagement 29.45% หรือมียอด engagemant 207028964 รองลงมาจะเป็นบัญชีที่เกี่ยวกับยูทูปเบอร์ที่ทำงานคนเดียวมียอด engagement 
22.11% หรือมียอด engagemant 155410835 และทำงานเป็นทีมมียอด engagement 18.43% หรือมียอด engagemant 129548974 ตามลำดับ ยอดfan บัญชีที่มีมากสุดเป็นบัญชีที่เกี่ยวกับนักแสดงหญิง มียอด engagement 35.87% หรือมียอด engagemant 14797155 
รองลงมาคือบัญชีของยูทูปเบอร์เดี่ยว มียอด engagement 31.69% หรือมียอด engagemant 13073557 แล้วก็ทีม มียอด engagement 15.25% หรือมียอด engagemant 6294303 ตามลำดับเมือเทียบยอด Engagement กับยอด Fan พบว่ากลุ่มบัญชีนักแสดงหญิงมียอดผู้ติดตามเยอะสุดเหมือนกัน นอกจากนี้จำนวน influencer ที่เยอะสุดคือ influecer ของนักแสดงหญิงเช่นกัน
เมื่อเทียบเป็นราย User พบว่า User Twitter ที่โพสเกี่ยวกับการขายของมีโอกาสที่จะได้ Engagement สูงที่สุด ในขณะที่บัญชี เกี่ยวกับ youtuber มีโอกาสที่จะได้ยอด follow สูงสุด
อย่างไรก็ตามการดูผลลัพธ์โดย Point จะไม่ค่อยมีประสิทธิภาพเนื่องจากจำนวน User ในแต่ละประเภทน้อยเกินไป อย่างเช่น บัญชีเกี่ยวกับการขายของ หรือ บัญชีเกี่ยวกับการโพสรูปเด็ก มีจำนวน User แค่ 1 User เท่านั้น ทำให้จำนวน Engagement อาจจะเยอะกว่า User กลุ่มอื่นที่มีจำนวน User มากกว่า

***ผลลัพธ์ Wordcloud*** จะเห็นได้ว่า wordcloud เกือบที้งหมดจะเกี่ยวกับขายของหมดเลยซึ่ง Wordcloud จะมีปัญหากับ Platform IG ตรงที่ว่า Platform IG ส่วนใหญ่จะลงเกี่ยวกับรูปซึ่งอาจจะไม่ได้ใช้คำกันมากนัก โดยการสรุปว่า Platform IG ส่วนใหญ่จะทำเกี่ยวกับการขายของคงจะไม่ค่อยมีประสิทธิภาพนัก ดังนั้นดีที่สุดควรอิงผลลัพธ์จากการดูว่า influencer ทำอะไรเป็นหลัก
## สรุป
![dekd](https://user-images.githubusercontent.com/83722061/117236291-9bd65b80-ae52-11eb-9172-d83ee38bc07e.PNG)


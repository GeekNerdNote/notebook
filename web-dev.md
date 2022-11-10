# Web Development

Website Development ที่เป็นมิตรสำหรับทุกคน

ซึ่งใน Guide จะแบ่งออกเป็น 3 ส่วนคือ

- [Beginner](#beginner)
- [Intermediate](#intermediate)
- [Expert](#expert)


## How Web work
## Beginner

ถ้าคุณเป็นมือใหม่ นี่คือสิ่งที่คุณขาดไม่ได้ ถ้าคุณข้าม Beginner นี้ไป ขั้นต่อๆไปคุณจะไม่เข้าใจ แนะนำให้เริ่มจากที่นี่ก่อน ว่า "Web มันทำงานยังไง" เพื่อรู้พื้นฐานการทำงานของ Website

- [How Web Work](How-Web-Work/README.md)

็HTML, CSS และ JS คือภาษาที่ run อยู่บน Web Browser ทั้ง 3 ทำงานร่วกันแต่ก็มีจุดประสงค์ของมันเองที่แตกต่างกัน

![HTML, CSS, JS](media/image/html-css-javascript-905348.png)

- [html](html.md) เปรียบเหมือนการร่างและวางโครงสร้าง content ต่างๆ ของ Web
- [CSS] เพื่อเพิ่มความสวยงาน และ สไตล์ต่างๆ
- [JS] เพื่อเพิ่ม interactive ให้กับ User

ยกตัวอย่างเช่น:

เราสามารถที่จะ บอก text นี้ว่าเป็น paragraph โดยใช้ HTML

```html
<p id="paragraph">This is a paragraph.</p>
```

แล้วเราสามารถที่จะแต่งสไตล์ต่างๆให้กับ component นี้ได้โดยใช้ CSS

```css
p {
  font-size: large;
}
```

และสามารถใส่ feature และ function ในที่นี้คือให้ User กดเข้าไปที่ปุ่มแล้วเปลี่ยน content ด้านในของ `<p>` เข้าไปโดยใช้ JS

```js
function ClickMe() {
  document.getElementById("paragraph").innerHTML = "You clicked me";
}

const myBtn = document.getElementById("myBtn");
myBtn.addEventListener("click", ClickMe);
```

เอาทั้ง 3 อย่างมารวมกันเป็น Web Page หนึ่ง จะได้แบบนี้

```html
<!DOCTYPE html>

<html>
  <head>
    <style>
      p {
        font-size: large;
      }
    </style>
  </head>

  <body>
    <button id="myBtn">Try it</button>

    <p id="paragraph">This is a paragraph.</p>

    <script>
      function ClickMe() {
        document.getElementById("paragraph").innerHTML = "You clicked me";
      }

      const myBtn = document.getElementById("myBtn");
      myBtn.addEventListener("click", ClickMe);
    </script>
  </body>
</html>
```

[Simple Web](source/html/index.html)

ซึ่งจะเห็นได้ว่าทั้ง 3 อย่างนี้ มีหน้าที่แตกต่างกัน แต่ทำงานร่วมกัน ซึ่ง website ส่วนใหญ่(เกือบทั้งโลกของ Web) จะใช้ทั้ง 3 ตัวในการแสดงผลของ Web

> การเข้าใจว่างทั้ง 3 ตัวนั้น เกี่ยวข้องกันยังไง นั้นเป็นก้าวแรกสำหรับการพัฒนาเว็ปเบื้องต้น

### Web development skill you really need

การเรียน HTML, CSS, JS นั้นเป็นแค่ "prerequisite" เพื่อที่จะเป็น Prof. Web Dev สกิลที่คุณต้องควรมีด้วยคือ

- Organizing HTML, into reusable templates
- Standing up Web server and Cloud 
- Design Patterns and Architect for web
- Deployment your website
- Version Control
- Pointing a Domain name for your server

การที่จะจัดการกับ Complexities ที่เกิดจากการตั้งค่า และ Configs ต่างๆ ใน "Environment"  เพื่อจัดระเบียบ File & Folder เพื่อที่ทำให้ ช่วง Dev & Deploy นั้นเป็นระเบียบไม่ยุ่งเหยิง

![WebHTML](media\image\languages-vs-web-dev-b849db.png)

### Tools for Web Development

สำหรับการพัฒนา web การมี Tools ที่ใช่ จะทำให้การพัฒนานั้นรวดเร็วมากขึ้น ซึ่งมี 2 ที่เป็นขั้นต่ำเลยคือ

- [Code & Text Editor]
- [Web Browser]

Basic Workflow คือ Write Code ใน Code & Text Editor แล้วไปแสดงผลแบบ Local ที่ Web Browser เพื่อที่จะดูผลลัพท์ Web ที่คุณเขียนขึ้นมา

การที่คุณจะพัฒนา Web ขึ้นมาจริงๆ คุณจะรู้ว่า การมี Code & Text Editor และ Web Browser แค่ไม่พอต่อการพัฒนา (พัฒนาได้ แต่ความล่าช้าจะช้ามากกกกกกก) การที่คุณจะหา Tools, Libraries, Framework เพิ่มมันจะไม่ใช่เรื่องแปลกในทำ Software Development

> การใช้ Tools อื่นๆ มันเป็นเรื่องที่ดีในการพัฒนา แต่ก็ไม่ควรมองข้างเรื่อง Fundamental ต่างๆ เพราะพื้นฐานที่ดีจะทำให้คุณเข้าใจสิ่งต่างๆมากขึ้น เมื่อเจอปัญหานั้น. Complexity ขึ้น


### Fundamental is the best of learning process

ในปัจจุบันนั้น Tools หรือ libray ต่างๆ มีเยอะแยะจนนับไม่ถ้วน หลายคนอาจจะเริ่มจากการใช้ tools เลย ซึ่งในความคิดเห็นส่วนตัว การเริ่มเรียนรู้ Tools โดยไม่มีพื้นฐาน มันเหมือนกันการไปสร้างตึกแต่ไม่มีความรู้ด้าน Engineering และ Architect 

ผมเองก็เคยเป็นแบบบนั้นมาก่อน คิดว่าการที่เรียนรู้ Tools ก่อนจะทำให้เราสร้าง Project เร็วขึ้น แต่ความเป็นจริง คุณจะสร้าง Project ไม่ได้ด้วยซ้ำ เพราะคุณไม่รู้ว่ามันทำงานยังไง

Tutorial นี้จะเริ่มสอน HTML, CSS, JS ก่อนแล้วจามด้วย Framework และ Library ทีหลัง

## Intermediate

### Roles of Web Development

- Front-End
- Back-End
- Full-Stack



## Expert

### DevOps

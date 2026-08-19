# Ex03 To-Do List using JavaScript
## Date:19-08-2026

## AIM
To create a To-do Application with all features using JavaScript.

## ALGORITHM
### STEP 1
Build the HTML structure (index.html).

### STEP 2
Style the App (style.css).

### STEP 3
Plan the features the To-Do App should have.

### STEP 4
Create a To-do application using Javascript.

### STEP 5
Add functionalities.

### STEP 6
Test the App.

### STEP 7
Open the HTML file in a browser to check layout and functionality.

### STEP 8
Fix styling issues and refine content placement.

### STEP 9
Deploy the website.

### STEP 10
Upload to GitHub Pages for free hosting.

## PROGRAM
# index.html
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <link rel="icon" href="%PUBLIC_URL%/favicon.ico" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <meta name="theme-color" content="#000000" />
    <meta
      name="description"
      content="Web site created using create-react-app"
    />
    <link rel="apple-touch-icon" href="%PUBLIC_URL%/logo192.png" />
    <!--
      manifest.json provides metadata used when your web app is installed on a
      user's mobile device or desktop. See https://developers.google.com/web/fundamentals/web-app-manifest/
    -->
    <link rel="manifest" href="%PUBLIC_URL%/manifest.json" />
    <!--
      Notice the use of %PUBLIC_URL% in the tags above.
      It will be replaced with the URL of the `public` folder during the build.
      Only files inside the `public` folder can be referenced from the HTML.

      Unlike "/favicon.ico" or "favicon.ico", "%PUBLIC_URL%/favicon.ico" will
      work correctly both with client-side routing and a non-root public URL.
      Learn how to configure a non-root public URL by running `npm run build`.
    -->
    <title>React App</title>
  </head>
  <body>
    <noscript>You need to enable JavaScript to run this app.</noscript>
    <div id="root"></div>
    <!--
      This HTML file is a template.
      If you open it directly in the browser, you will see an empty page.

      You can add webfonts, meta tags, or analytics to this file.
      The build step will place the bundled scripts into the <body> tag.

      To begin the development, run `npm start` or `yarn start`.
      To create a production bundle, use `npm run build` or `yarn build`.
    -->
  </body>
</html>

```
# ToDo.jsx
   
  }




    return (<>
    <header className="hero">My Task List</header>
    <div className="container">
        <div className="row">
            <div className="item">
                <label>Add Task</label>
            </div>
             <div className="item">
                <input type="text"
                title="Enter task here..."
                placeholder="Enter task here..."
                ref={taskTextBox} />
             </div>
             
        </div>

         <div className="row">
            <div className="item">
                <label>Add Desc</label>
            </div>
             <div className="item">
                <textarea 
                placeholder="Enter task description here..."
                ref={taskDescBox}
                ></textarea>
             </div>
        </div>

        <div className="row">
            <div className="item">
                <label>Task Type</label>
            <div className="item">
                <label>Due Date</label>
            </div>
             <div className="item">
                <input type="date"
                ref={taskDateBox}
                 defaultValue={new Date().toISOString().split('T')[0]} />
             </div>
        </div>
        <div className="row">
            <div className="item">
                <label>Time</label>
            </div>
             <div className="item">
                <input type="time"
                ref={taskTimeBox}
                 defaultValue={new Date().toTimeString().slice(0, 5)} />
             </div>
        </div>
        <div className="row">
            <div className="item">
                
            </div>
             <div className="item">
                <button onClick={handleAddTask}>Add</button>
             </div>
        </div>
    </div>
    <div>
        <h2>Task List</h2>
        <ul>
            {taskList.map((task, index) => (
                <li key={index}>
                    <strong>{task.taskName}</strong> - {task.taskDesc} ({task.taskType}) - {task.taskDate} at {task.taskTime}
                </li>
            ))}
        </ul>
    </div>
    </>)
}

export default ToDo;
```

# style.css

/* ==========================
   Reset
========================== */

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Segoe UI,Tahoma,Geneva,Verdana,sans-serif;
}

body{
    background:var(--background);
}

/* ==========================
   Hero
========================== */

.hero{

    background:linear-gradient(135deg,var(--primary),var(--secondary));
    color:white;

    text-align:center;

    font-size:34px;
    font-weight:bold;

    padding:30px;

    letter-spacing:1px;

    box-shadow:0 5px 15px rgba(0,0,0,.15);

}

/* ==========================
   Container
========================== */

.container{

    width:min(900px,92%);
    margin:40px auto;

    background:var(--surface);

    border-radius:var(--radius);

    padding:35px;

    box-shadow:var(--shadow);

}

/* ==========================
    flex:3;

}

/* ==========================
   Labels
========================== */

label{

    color:var(--text);

    font-weight:600;

    font-size:16px;

}

/* ==========================
   Inputs
========================== */

input,
textarea,
select{

    width:100%;

    padding:12px 15px;

    border:1px solid var(--border);

    border-radius:10px;

    font-size:15px;

    outline:none;

    transition:.3s;

    background:white;

}

textarea{

    min-height:120px;

    resize:vertical;

}

input:focus,
textarea:focus,
select:focus{
  border-color:var(--primary);
    font-size:16px;

    font-weight:bold;

    border-radius:10px;

    cursor:pointer;

    transition:.3s;

}

button:hover{

    transform:translateY(-2px);

    box-shadow:0 10px 20px rgba(37,99,235,.25);

}

button:active{

    transform:scale(.98);

}

/* ==========================
   Placeholder
========================== */

::placeholder{

    color:#999;

}

/* ==========================
   Responsive
========================== */

@media(max-width:768px){

    .hero{

        font-size:28px;

        padding:22px;

    }

    .container{

        padding:25px;

    }

    .row{

        flex-direction:column;

        align-items:flex-start;

        gap:10px;

    }

    .item{

        width:100%;

    }

    button{

        width:100%;

    }

}

@media(max-width:480px){

    .hero{

        font-size:24px;

    }

    .container{

        padding:20px;

    }

    label{

        font-size:15px;

    }

}
```


## OUTPUT

<img width="1919" height="1102" alt="Screenshot 2026-08-09 212218" src="https://github.com/user-attachments/assets/72dba2f0-d473-4af5-84fc-5ec9b20b2ff7" />

## RESULT
The program for creating To-do list using JavaScript is executed successfully.









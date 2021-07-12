---

title: '[web] animation'
excerpt: HTML, CSS animation.


categories:
    - web

tags:
    - [html, css, web]


toc: true
toc_sticky: true


date: 2021-04-30
last_modified_at: 2021-04-30

---

__*Make a animation by using HTML & CSS*__

 ***

<iframe width="855" height="500" src="https://www.youtube.com/embed/HUGenLjVHLE" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

# index.html

```
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Animation Assignment - NomadCoders</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="circle">●&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;●&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;●</div>
    <div id="bar_container">
        <span>
            <div class="bar"></div>
            <div class="bar"></div>
            <div class="bar"></div>
            <div class="bar"></div>
            <div class="bar"></div>
        </span>
    </div>
</body>
</html>

```


# style.css

```

body{
    height: 100vh;
    background-color:rgb(126, 186, 189);
    display: flex;
    position: relative;
    justify-content: space-evenly;
    align-items: center;
    flex-direction: column;
}

@keyframes rotate_circle{
    from{
        transform: rotateZ(0);
    }
    to{
        transform: rotateZ(360deg);
    }
}

@keyframes wave_bar{
    0%{
        transform: scaleY(0.8);
    }
    50%{
        transform: scaleY(2);
    }
    100%{
        transform: scaleY(1);
    }
}

#circle{
    color: white;
    display: flex;
    animation: rotate_circle 2.5s ease-in-out infinite;
}

#bar_container{
    display: flex;
}

.bar{
    display: inline-block;
    width: 8px;
    height: 40px;
    background-color: white;
    margin: 0.5px;
    border-radius: 10px;
}


.bar:first-child{
    animation: wave_bar 0.8s cubic-bezier(0.445, 0.050, 0.550, 0.950) infinite;   
    animation-delay: 0s;
}
.bar:nth-child(2){
    animation: wave_bar 0.8s cubic-bezier(0.445, 0.050, 0.550, 0.950) infinite;
    animation-delay: 0.15s;
}
.bar:nth-child(3){
    animation: wave_bar 0.8s cubic-bezier(0.445, 0.050, 0.550, 0.950) infinite;
    animation-delay: 0.3s;
}
.bar:nth-child(4){
    animation: wave_bar 0.8s cubic-bezier(0.445, 0.050, 0.550, 0.950) infinite;
    animation-delay: 0.45s;
}
.bar:last-child{
    animation: wave_bar 0.8s cubic-bezier(0.445, 0.050, 0.550, 0.950) infinite;
    animation-delay: 0.6s;
}

```

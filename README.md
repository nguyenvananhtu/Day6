<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="Day6.css">
    <title>Day6</title>
</head>
    <style>
        *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body{
    background-image: url(https://blogchiasekienthuc.com/wp-content/uploads/2022/12/hinh-nen-may-tinh-fantasy-4k-blogchiasekienthuc.com-1.png);
    background-repeat: no-repeat;
    background-size: cover;
    height: 100vh;
    color: rgb(253, 251, 251);
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-family: Arial, Helvetica, sans-serif;
}

.alert{
    font-size: 40px;
    color:white;
    background: rgb(181,126,220);;
    border-radius: 12px;
    padding: 10px 40px;
    border: none;
    outline: none;
    font-weight: 600px;
}

.box .result{
    height: 250px;
    width: 250px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 70px;
    font-weight: 600;
    margin: auto;
    margin-bottom: 60px;
    font-size: 35px;
    border: 5px solid rgb(251, 251, 252);
}

.card{
    width: 300px;
    background: white;
    border-radius: 10px;
    margin: 20px;
    overflow: hidden;
}

.card p{
    padding: 10px;
    text-align: center;
    color: black;
    font-size: 20px;
}

.card p:first-child{
    background:  linear-gradient(to right, #b827fc 0%, #2c90fc 25%, #456405 50%, #b68f24 75%, #fd1892 100%);
    color: white;
}

.detail{
    display: flex;
}

.hide{
    display: none;
}
    </style>
<body>
    <button class="alert  ">Press Any Key</button>
    <div class="box hide">
        <div class="result">40</div>
        <div class="detail">
            <div class="card key">
                <p>Key</p>
                <p>0</p>
            </div>

            <div class="card location">
                <p>Location</p>
                <p>0</p>
            </div>

            <div class="card which">
                <p>Which</p>
                <p>0</p>
            </div>

            <div class="card code">
                <p>Code</p>
                <p>0</p>
            </div>
        </div>
    </div>
    <script>
        var eKey = document.querySelector('.card.key p:last-child')
        var eLocation = document.querySelector('.card.location p:last-child')
        var eWhich = document.querySelector('.card.which p:last-child')
        var eCode = document.querySelector('.card.code p:last-child')
        var alert = document.querySelector('.alert')
        var box = document.querySelector('.box')
        var result = document.querySelector('.result')

        document.addEventListener('keydown', e => {

            eKey.innerText = e.key
            eLocation.innerText = e.location
            eWhich.innerText = e.which
            eCode.innerText = e.code
            result.innerHTML = e.code

            alert.classList.add('hide')
            box.classList.remove('hide')
        })
    </script>
</body>

</html>

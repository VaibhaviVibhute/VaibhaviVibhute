<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
</head>
<style>
    body{
        margin: 0px auto;
        padding: 0;
        box-sizing: border-box;
        display: flex;
        justify-content: center;
        align-items: center;
    }
    #main_box{
        height: 575px;
        width: 350px;
        /* border: 1px solid black; */
        margin-top: 50px;
        display: flex;
        flex-direction: column;
        box-shadow: 3px 5px 6px gray;
    }
    #container{
        height: 390px;
        width: 350px;
        /* border: 1px solid black; */
        /* margin-top: 180px; */
    }
    .box{
        height: 60px;
        width: 350px;
        /* border: 1px solid black; */
        margin-top: 20px;
    }
    .opt{
        height: 60px;
        width: 60px;
        font-size: 20px;
        font-weight: 500;
        margin-left: 20px;
        border-radius: 50%;
        box-shadow: 1px 0px 0px black;
        background-color: white;
    }
    .button{
        height: 60px;
        width: 60px;
        font-size: 20px;
        font-weight: 500;
        margin-left: 20px;
        border-radius: 50%;
        box-shadow: 1px 0px 0px black;
        background-color: white;
    }
    #button19{
        width: 130px;
        border: none;
        font-size: 28px;
        border-radius: 0%;
        margin-left: 25px;
        border-top-right-radius: 50px;
        border-bottom-right-radius: 50px;
        border-bottom-left-radius: 50px;
        border-top-left-radius: 50px;
        background-color: green;
        border: none;
        box-shadow: 1px 0px 0px black;
        color: aliceblue;
    }
    #box1{
        margin-top: 0%;
    }

    #inp{
        height: 180px;
        width: 350px;
        /* border: 1px solid black; */
    }
    #ans{
        height: 165px;
        width: 335px;
        /* border: 1px solid black; */
        border-color: rgb(235, 231, 231);
        background-color: rgb(235, 231, 231);
        text-align: right;
        margin-left: 5px;
        margin-top: 3px;
        font-size: 25px;
        /* margin-left: px; */
        /* margin-top: 2px; */
    }
   
</style>
<body>
    <div id="main_box">
        <div id="inp">
                <input type="text" id="ans" class="ans1">
        </div>
        <div id="container">
            <div class="box" id="box1">
                <input type="button" class="button" id="button1" value="C" onclick="clrscr()">
                <input type="button" class="opt" id="button2" value="+/-">
                <input type="button" class="button" id="button3" value="DEL" onclick="pressClear()">
                <input type="button" class="opt" id="button4" value="/" onclick="getvalue('/')">
            </div>
            <div class="box" id="box2">
                <input type="button" class="button" id="button5" value="7" onclick="getvalue('7')">
                <input type="button" class="button" id="button6" value="8" onclick="getvalue('8')">
                <input type="button" class="button" id="button7" value="9" onclick="getvalue('9')">
                <input type="button" class="opt" id="button8" value="*" onclick="getvalue('*')">
            </div>
            <div class="box" id="box3">
                <input type="button" class="button" id="button9" value="4"onclick="getvalue ('4')">
                <input type="button" class="button" id="button10" value="5"onclick="getvalue('5')">
                <input type="button" class="button" id="button11" value="6"onclick="getvalue('6')">
                <input type="button" class="opt" id="button12" value="-" onclick="getvalue('-')">
            </div>
            <div class="box" id="box4">
                <input type="button" class="button" id="button13" value="1" onclick="getvalue('1')">
                <input type="button" class="button" id="button14" value="2" onclick="getvalue('2')">
                <input type="button" class="button" id="button15" value="3" onclick="getvalue('3')">
                <input type="button" class="opt" id="button16" value="+" onclick="getvalue('+')">
            </div>
            <div class="box" id="box5">
                <input type="button" class="button" id="button17" value="0" onclick="getvalue('0')">
                <input type="button" class="button" id="button18" value="." onclick="getvalue('.')">
                <input type="button" class="opt" id="button19" value="=" onclick="getresult('=')">
            </div>
        </div>
    </div>

    <script>
        function pressClear() {
  			var str = document.getElementById("ans").value
            str = str.slice(0,-1);
            document.getElementById("ans").value = str;
		}

        function clrscr() {
            document.getElementById("ans").value=""
        }
        function getvalue(val) {
            document.getElementById("ans").value+=val
            return val
        }
        function getresult() {
            let x=document.getElementById('ans').value
            let y=eval(x);
            document.getElementById('ans').value=y
            return y;
        }
    </script>
</body>
</html>

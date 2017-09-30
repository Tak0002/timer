/* 
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */


var checker;
var timer;
var timerMax = 1000 * 25 * 60;
window.onload = function(){
   checker1 = setInterval('message()',10000);
   checker2 = setInterval('display()',1000);
};

var isTimerWorking = false;
var startTime = 0;
var leftTime = 0;

function message(){
    if (!isTimerWorking) {
        alert('タイマーをセットしてください');
    }
    // 一定時間ごとにやりたい処理
}

function display(){
    if (isTimerWorking) {
        var date = new Date();
        var now = date.getTime();
        var diff = now - startTime;
        var leftTimeSec = Math.floor(( leftTime - diff) / 1000 );
        var min =  Math.floor( leftTimeSec/60 );
        var sec = leftTimeSec%60;
        console.log(min + ':' + sec );
    }
}


function start(){
    if (isTimerWorking) {
        return;
    }
    isTimerWorking = true;
    if (startTime === 0 || leftTime === 0){
        leftTime = timerMax;
    } else {
        console.log('err');
    }
    var date = new Date();
    startTime = date.getTime();
    timer = setTimeout('finish()',leftTime); // 1000ミリ秒ごとに実行したい処理hoge()を登録
    alert('開始しました')

}

function pause(){
    clearInterval('finish()');
    isTimerWorking = false;
    var date = new Date();
    var now = date.getTime();
    var diff = now - startTime;
    leftTime = leftTime - diff;
    alert('中止しました')
}


function stop(){
    clearInterval('finish()');
    isTimerWorking = false;
    startTime = 0;
    leftTime = 0;
}

function finish(){
    isTimerWorking = false;
    startTime = 0;
    leftTime = 0;
    alert('終了しました')
}





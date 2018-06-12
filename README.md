# jeDate源码更改（使之更精小） jeDate

效果如下：
![](images/img.gif)

更改的CSS代码：
```
/* CSS Document */
.jedatebox{
    /*width:270px;*/
    width:226px;
    height:auto;
    font-family:'PingFangSC-Light',
    'PingFang SC','Segoe UI','Lucida Grande',
    'NotoSansHans-Light','Microsoft YaHei',
    '\5FAE\8F6F\96C5\9ED1', STHeiti,
    'WenQuanYi Micro Hei', SimSun,
    sans-serif;
    font-size:12px;
    cursor:default;
    margin: 0;padding: 0;
    border-radius: 4px;
    overflow: hidden;
}
.jedatebox *{-webkit-box-sizing:border-box;-moz-box-sizing:border-box;box-sizing:border-box;font-style:normal;font-family:'PingFangSC-Light','PingFang SC','Segoe UI','Lucida Grande','NotoSansHans-Light','Microsoft YaHei', '\5FAE\8F6F\96C5\9ED1', STHeiti, 'WenQuanYi Micro Hei', SimSun, sans-serif;font-size:12px;}
.jedatebox ul,.jedatebox ol,.jedatebox li,.jedatebox dl{list-style-type:none;font-style:normal;font-weight: 300;}
.jedatebox .jedateym .prev{background-image: url("data:image/gif;base64,R0lGODlhBQAJAIABAP///////yH/C1hNUCBEYXRhWE1QPD94cGFja2V0IGJlZ2luPSLvu78iIGlkPSJXNU0wTXBDZWhpSHpyZVN6TlRjemtjOWQiPz4gPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iQWRvYmUgWE1QIENvcmUgNS41LWMwMjEgNzkuMTU1NzcyLCAyMDE0LzAxLzEzLTE5OjQ0OjAwICAgICAgICAiPiA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPiA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIiB4bWxuczp4bXA9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC8iIHhtbG5zOnhtcE1NPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvbW0vIiB4bWxuczpzdFJlZj0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL3NUeXBlL1Jlc291cmNlUmVmIyIgeG1wOkNyZWF0b3JUb29sPSJBZG9iZSBQaG90b3Nob3AgQ0MgMjAxNCAoV2luZG93cykiIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6MEIxREZCQ0E3NTFCMTFFNkIxRDFEQzhDMDRCNjUxNDYiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6MEIxREZCQ0I3NTFCMTFFNkIxRDFEQzhDMDRCNjUxNDYiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDowQjFERkJDODc1MUIxMUU2QjFEMURDOEMwNEI2NTE0NiIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDowQjFERkJDOTc1MUIxMUU2QjFEMURDOEMwNEI2NTE0NiIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/PgH//v38+/r5+Pf29fTz8vHw7+7t7Ovq6ejn5uXk4+Lh4N/e3dzb2tnY19bV1NPS0dDPzs3My8rJyMfGxcTDwsHAv769vLu6ubi3trW0s7KxsK+urayrqqmop6alpKOioaCfnp2cm5qZmJeWlZSTkpGQj46NjIuKiYiHhoWEg4KBgH9+fXx7enl4d3Z1dHNycXBvbm1sa2ppaGdmZWRjYmFgX15dXFtaWVhXVlVUU1JRUE9OTUxLSklIR0ZFRENCQUA/Pj08Ozo5ODc2NTQzMjEwLy4tLCsqKSgnJiUkIyIhIB8eHRwbGhkYFxYVFBMSERAPDg0MCwoJCAcGBQQDAgEAACH5BAEAAAEALAAAAAAFAAkAAAIMjAMHidsLXTRQMVoAADs=");}
.jedatebox .jedateym .next{background-image: url("data:image/gif;base64,R0lGODlhBQAJAIABAP///////yH/C1hNUCBEYXRhWE1QPD94cGFja2V0IGJlZ2luPSLvu78iIGlkPSJXNU0wTXBDZWhpSHpyZVN6TlRjemtjOWQiPz4gPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iQWRvYmUgWE1QIENvcmUgNS41LWMwMjEgNzkuMTU1NzcyLCAyMDE0LzAxLzEzLTE5OjQ0OjAwICAgICAgICAiPiA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPiA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIiB4bWxuczp4bXA9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC8iIHhtbG5zOnhtcE1NPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvbW0vIiB4bWxuczpzdFJlZj0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL3NUeXBlL1Jlc291cmNlUmVmIyIgeG1wOkNyZWF0b3JUb29sPSJBZG9iZSBQaG90b3Nob3AgQ0MgMjAxNCAoV2luZG93cykiIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6MUJDNTNBNTY3NTFCMTFFNkJGMjJFRDQ2NDZCQ0RDMDAiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6MUJDNTNBNTc3NTFCMTFFNkJGMjJFRDQ2NDZCQ0RDMDAiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDoxQkM1M0E1NDc1MUIxMUU2QkYyMkVENDY0NkJDREMwMCIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDoxQkM1M0E1NTc1MUIxMUU2QkYyMkVENDY0NkJDREMwMCIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/PgH//v38+/r5+Pf29fTz8vHw7+7t7Ovq6ejn5uXk4+Lh4N/e3dzb2tnY19bV1NPS0dDPzs3My8rJyMfGxcTDwsHAv769vLu6ubi3trW0s7KxsK+urayrqqmop6alpKOioaCfnp2cm5qZmJeWlZSTkpGQj46NjIuKiYiHhoWEg4KBgH9+fXx7enl4d3Z1dHNycXBvbm1sa2ppaGdmZWRjYmFgX15dXFtaWVhXVlVUU1JRUE9OTUxLSklIR0ZFRENCQUA/Pj08Ozo5ODc2NTQzMjEwLy4tLCsqKSgnJiUkIyIhIB8eHRwbGhkYFxYVFBMSERAPDg0MCwoJCAcGBQQDAgEAACH5BAEAAAEALAAAAAAFAAkAAAIMRB5gp9v2YlJsJRQKADs=");}
.jedatebox .jedateym .pndrop{
    width:14px;
    /*height:40px; */
    height:30px;
    overflow:hidden;
    display: inline-block;
    position:relative;
    vertical-align: top;
    background-repeat: no-repeat;
    background-position: center center;
    background-image: url("data:image/gif;base64,R0lGODlhCQAFAIABAP///////yH/C1hNUCBEYXRhWE1QPD94cGFja2V0IGJlZ2luPSLvu78iIGlkPSJXNU0wTXBDZWhpSHpyZVN6TlRjemtjOWQiPz4gPHg6eG1wbWV0YSB4bWxuczp4PSJhZG9iZTpuczptZXRhLyIgeDp4bXB0az0iQWRvYmUgWE1QIENvcmUgNS41LWMwMjEgNzkuMTU1NzcyLCAyMDE0LzAxLzEzLTE5OjQ0OjAwICAgICAgICAiPiA8cmRmOlJERiB4bWxuczpyZGY9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkvMDIvMjItcmRmLXN5bnRheC1ucyMiPiA8cmRmOkRlc2NyaXB0aW9uIHJkZjphYm91dD0iIiB4bWxuczp4bXA9Imh0dHA6Ly9ucy5hZG9iZS5jb20veGFwLzEuMC8iIHhtbG5zOnhtcE1NPSJodHRwOi8vbnMuYWRvYmUuY29tL3hhcC8xLjAvbW0vIiB4bWxuczpzdFJlZj0iaHR0cDovL25zLmFkb2JlLmNvbS94YXAvMS4wL3NUeXBlL1Jlc291cmNlUmVmIyIgeG1wOkNyZWF0b3JUb29sPSJBZG9iZSBQaG90b3Nob3AgQ0MgMjAxNCAoV2luZG93cykiIHhtcE1NOkluc3RhbmNlSUQ9InhtcC5paWQ6NDRERDNEMjA3NTFCMTFFNkE0QjFBRTExMDY2QjY5MEUiIHhtcE1NOkRvY3VtZW50SUQ9InhtcC5kaWQ6NDRERDNEMjE3NTFCMTFFNkE0QjFBRTExMDY2QjY5MEUiPiA8eG1wTU06RGVyaXZlZEZyb20gc3RSZWY6aW5zdGFuY2VJRD0ieG1wLmlpZDo0NEREM0QxRTc1MUIxMUU2QTRCMUFFMTEwNjZCNjkwRSIgc3RSZWY6ZG9jdW1lbnRJRD0ieG1wLmRpZDo0NEREM0QxRjc1MUIxMUU2QTRCMUFFMTEwNjZCNjkwRSIvPiA8L3JkZjpEZXNjcmlwdGlvbj4gPC9yZGY6UkRGPiA8L3g6eG1wbWV0YT4gPD94cGFja2V0IGVuZD0iciI/PgH//v38+/r5+Pf29fTz8vHw7+7t7Ovq6ejn5uXk4+Lh4N/e3dzb2tnY19bV1NPS0dDPzs3My8rJyMfGxcTDwsHAv769vLu6ubi3trW0s7KxsK+urayrqqmop6alpKOioaCfnp2cm5qZmJeWlZSTkpGQj46NjIuKiYiHhoWEg4KBgH9+fXx7enl4d3Z1dHNycXBvbm1sa2ppaGdmZWRjYmFgX15dXFtaWVhXVlVUU1JRUE9OTUxLSklIR0ZFRENCQUA/Pj08Ozo5ODc2NTQzMjEwLy4tLCsqKSgnJiUkIyIhIB8eHRwbGhkYFxYVFBMSERAPDg0MCwoJCAcGBQQDAgEAACH5BAEAAAEALAAAAAAJAAUAAAIKhH+BGYoNGWxgFgA7");
}
.jedatebox .jedateym .prev,.jedatebox .jedateym .next{
    width:15%;
    /*height:40px;*/
    height:30px;
    float:left;
    display:block;
    text-align: center;
    background-repeat: no-repeat;
    background-position: center center;
}
.jedatebox em,.jedatebox i{
    /*height:40px;*/
    height:30px;
    margin: 0;
    padding: 0;
    font-style:normal;
    display:inline-block;
    /*font-size: 16px;*/
    font-size: 13px;
}
.jedatetipscon{color:#000; float:left; overflow:hidden;background-color: #FFFEF4; line-height:22px;padding:6px;border: 1px rgb(247, 206, 57) solid;font-style:normal;font-family:'PingFangSC-Light','PingFang SC','Segoe UI','Lucida Grande','NotoSansHans-Light','Microsoft YaHei', '\5FAE\8F6F\96C5\9ED1', STHeiti, 'WenQuanYi Micro Hei', SimSun, sans-serif;font-size:12px;font-weight: 300;}
.jedatetipscon p{padding: 0;margin: 0;}
.jedatetipscon p.red{color: #ff0000;}

.jedatebox .jedatehmscon::-webkit-scrollbar{height:6px;width:6px;margin-right:5px;background: #f5f5f5;transition:all 0.3s ease-in-out;border-radius:0px}
.jedatebox .jedatehmscon::-webkit-scrollbar-track { -webkit-border-radius: 0px;border-radius: 0px;}
.jedatebox .jedatehmscon::-webkit-scrollbar-thumb{-webkit-border-radius: 0px;border-radius: 0px;background: rgba(0,0,0,0.5); }
.jedatebox .jedatehmscon::-webkit-scrollbar-thumb:hover{background:rgba(0,0,0,0.6)}
.jedatebox .jedatehmscon::-webkit-scrollbar-thumb:active{background:rgba(0,0,0,0.8)}
.jedatebox .jedatehmscon::-webkit-scrollbar-thumb:window-inactive {background: rgba(0,0,0,0.4);}
/* 蓝色风格 */
.jedateblue{
    /*border:1px #00A1CB solid;*/
    border:1px #41737f solid;
    background-color:#fff;
}
.jedateblue div,.jedateblue ol,.jedateblue ul,.jedateblue li,.jedateblue p,.jedateblue span{margin: 0;padding: 0;list-style-type:none;}
.jedateblue.dateshow{display:block;}
.jedateblue .jedatetop{
    width:100%;
    /*background: #00A1CB; */
    background: #41737f;
    color:#fff;
    overflow:hidden;
    text-align:center;
}
.jedateblue .jedateym{
    float:left;
    /*height:40px;*/
    height:30px;
    /*line-height:40px;*/
    line-height:30px;
}
.jedateblue .jedateym span{width:70%;padding: 0;float:left;text-align: center;text-overflow: ellipsis; display:block;}
.jedateblue .jedateym span input{width:100%;float:left;padding: 0;border:none;background-color:transparent;text-align: center;}
.jedateblue .jedateym .triangle{margin: 0;padding:0;font-style:normal;}
.jedateblue .jedateym .triangle:hover{background-color:#00B9E8;}
.jedateblue .jedatesety,.jedateblue .jedatesetm{
    width: 100%;
    position:absolute;
    left:0;
    /*top:40px;*/
    top:25px;
    bottom:0;
    background-color: #fff;
    z-index:50;
}
.jedateblue .jedatesety .ymdropul,.jedateblue .jedatesetm .ymdropul{
    width:100%;
    /*height:246px;*/
    height:160px;
    overflow:auto;
}
.jedateblue .jedatesety .ymdropul li{
    width:33.3%;
    float:left;
    text-align: center;
    /*height:49px;*/
    height:30px;
    /*line-height:49px;*/
    line-height:30px;
    /*font-size: 16px;*/
    font-size: 14px;
}
.jedateblue .jedatesety .ymdropul li.disabled{color:#bbb;}
.jedateblue .jedatesetm .ymdropul li{
    width:33.3%;
    float:left;
    text-align: center;
    /*height:60px;*/
    height:40px;
    /*line-height:60px;*/
    line-height:40px;
    /*font-size: 16px;*/
    font-size: 15px;
}
.jedateblue .jedatesetm .ymdropul li.disabled{color:#bbb;}
.jedateblue .jedatesety .ymdropul li.disabled:hover,.jedateblue .jedatesetm .ymdropul li.disabled:hover{background:#fff;}
.jedateblue .jedatesety .ymdropul li:hover,.jedateblue .jedatesetm .ymdropul li:hover{background: #F2F2F2;border-radius:4px;}
.jedateblue .jedatesety .ymdropul li.action,.jedateblue .jedatesetm .ymdropul li.action{
    /*background: #00A1CB;*/
    background: #41737f;
    color:#fff;
    border-radius:4px;
}
.jedateblue .jedatesety .ymdropul li.action:hover,.jedateblue .jedatesetm .ymdropul li.action:hover{background: #00A1CB;color:#fff;}
.jedateblue .jedatetopym p{overflow:auto; padding-top:4px;}
.jedateblue .jedatetopym p span{width:31%; margin:0 1.1%;background-color: #00A1CB;color: #fff;display: block;height:28px;line-height:28px; border-radius:5px;text-align:center;}
.jedateblue .jedatetopym p span.jedateymchri{
    background-color:#F0F0F0;
    color: #555;
    float:left;
    /*font-size: 16px;*/
    font-size: 12px;
}
.jedateblue .jedatetopym p span.jedateymchle{
    background-color: #F0F0F0;
    color: #555;
    float:left;
    /*font-size: 16px;*/
    font-size: 12px;
}
.jedateblue .jedatetopym p span.jedateymchok{
    /*background-color: #00A1CB;*/
    background: #41737f;
    color:#fff;
    float:right;
    font-size: 12px;
}

.jedateblue .jedayy,.jedateblue .jedaym{height:202px;overflow:auto; padding:5px;}
.jedateblue .jedayy li{width:33.3%;float:left;text-align: center;height:38px; line-height:38px;font-size: 14px;}
.jedateblue .jedayy li.action,.jedateblue .jedayy li.action:hover{background: #00A1CB;color:#fff;border-radius:4px;}
.jedateblue .jedayy li:hover{background: #F2F2F2;border-radius:4px;}
.jedateblue .jedayy li.disabled{ color:#bbb;}
.jedateblue .jedaym li{width:50%;float:left;text-align: center;height:32px; line-height:32px;font-size: 14px;}
.jedateblue .jedaym li.action,.jedateblue .jedaym li.action:hover{background: #00A1CB;color:#fff;border-radius:4px;}
.jedateblue .jedaym li:hover{background: #F2F2F2;border-radius:4px;}
.jedateblue .jedaym li.disabled { color: #bbb;  }
.jedateblue .jedaol{width:100%;overflow:auto;}
.jedateblue .jedaul{ padding:0px;overflow:auto;}
.jedateblue .jedaol li{
    width:14.28%;
    float:left;
    /*height:30px; */
    height:20px;
    /*line-height:30px;*/
    line-height:20px;
    text-align:center;
    position:relative;
    overflow:hidden;
}
.jedateblue .jedaul li{
    width:14.28%;
    float:left;
    /*height:36px;*/
    height:25px;
    text-align:center;
    position:relative;
    overflow:hidden;
    border-right: 1px #efefef solid;
    border-bottom: 1px #efefef solid;
}
.jedateblue .jedaul li .nolunar{
    /*line-height: 36px;*/
    line-height: 25px;
    /*font-size: 15px;*/
    font-size: 13px;
}
.jedateblue .jedaul li .solar{height:16px;line-height:16px;font-size: 14px;padding-top: 3px;display: block;}
.jedateblue .jedaul li .lunar{height:16px;line-height:16px;font-size: 12px;overflow:hidden;display: block;padding: 0 5px;}
.jedateblue .jedaol li.weeks{background:#f5f5f5;border-bottom: 1px solid #ddd;}
.jedateblue .jedaul li.action,.jedateblue .jedaul li.action:hover,.jedateblue .jedaul li.action .lunar{
    /*background: #00A1CB;*/
    background: #41737f;
    color:#fff;
}
.jedateblue .jedaul li.other,.jedateblue .jedaul li.other .nolunar,.jedateblue .jedaul li.other .lunar{color:#4DDBFF;}
.jedateblue .jedaul li.disabled,.jedateblue .jedaul li.disabled .nolunar,.jedateblue .jedaul li.disabled .lunar{ color:#bbb;}
.jedateblue .jedaul li.disabled:hover{background:#fff;}
.jedateblue .jedaul li:nth-child(7n){border-right:none;}
.jedateblue .jedaul li:hover{background: #F2F2F2;}
.jedateblue .jedaul li.red{ color:#ff0000;}
.jedateblue .jedaul li .marks{ width:5px; height:5px; background:#ff0000; -webkit-border-radius:50%;border-radius:50%; position:absolute; right:2px; top:4px;}
.jedateblue .jedaul li.action .marks{ width:5px; height:5px; background:#fff; -webkit-border-radius:50%;border-radius:50%; position:absolute; right:2px; top:4px;}

.jedateblue .jedatebot{
    /*height:34px;*/
    height:30px;
    /*line-height:34px; */
    line-height:30px;
    padding:0 3px 0 5px;
    overflow:hidden;
    background:#f5f5f5;
}
.jedateblue .jedatebot .jedatehms{
    /*border:1px #ddd solid;*/
    background-color: #fff;
    /*margin:0px 5% 3px 0;*/
    margin:0px 5% 0px 0;
    padding-left:1px;
    display:inline-block;
    overflow:hidden;
}
.jedateblue .jedatebot .botflex{
    width:50%;
    float:left;
    display: inline-block;
    margin:0;
    /*padding-top:3px;*/
    padding-top:4px;
    overflow:hidden;
}
.jedateblue .jedatebot .botflex li{
    /*width:32px;*/
    width:25px;
    float:left;
    text-align:center;
}
.jedateblue .jedatebot .botflex li input{
    width:100%;
    float:left;
    padding: 0;
    border:none;
    text-align: center;
    display:block;
    /*height:26px;*/
    height:22px;
    /*line-height:26px;*/
    line-height:22px;
    text-decoration: none;
    outline:none;
    -moz-outline:none;
    /*font-size: 14px;*/
    font-size: 12px;
    font-family:'Avenir Next',
    Avenir, 'Helvetica Neue',
    Helvetica, 'Lantinghei SC',
    'Hiragino Sans GB',
    'Microsoft YaHei',
    '\5FAE\8F6F\96C5\9ED1',
    STHeiti,
    'WenQuanYi Micro Hei',
    SimSun, sans-serif;
}
.jedateblue .jedatebot .botflex li input[disabled]{background-color: #f0f0f0;color: #aaa;}
.jedateblue .jedatebot .botflex i{
    width:12px;
    float:left;
    /*height:26px;*/
    height:22px;
    /*line-height:24px;*/
    line-height:22px;
    font-style:normal;
    display:block;
    text-align: center;
    background: #f2f2f2;
}
.jedateblue .jedatebot .jedatebtn{text-align:center;font-size: 12px;}
.jedateblue .jedatebot .jedatebtn span{
    /*width:31%;*/
    width:26%;
    float:right;
    /*margin:0 1.1%;*/
    margin:0 2.1%;
    /*background-color: #00A1CB;*/
    background: #41737f;
    color: #fff;
    display: block;
    /*height:28px;*/
    height:23px;
    /*line-height:28px;*/
    line-height:23px;
    border-radius:4px;
    text-align:center;
}

.jedateblue .jedateprophms{width: 100%;background: #FFF;}
.jedateblue .jedateproppos{position:absolute;left:0; top:0px;display:none;}
.jedateblue .jedatepropfix{display:block;}
.jedateblue .jedatepropcon{padding:40px 5px 5px 5px;background-color: #fff; overflow:hidden;position: relative;}
.jedateblue .jedatehmstitle{
    width:100%;
    height:40px;
    line-height:40px;
    position:absolute;
    left:0;
    top:0;
    /*background: #00A1CB;*/
    background: #41737f;
    color:#EEEEEE;
    overflow:hidden;
    text-align:center;
    font-size: 15px;
}
.jedateblue .jedateproptext{
    /*width:72px;*/
    width:60px;
    float:left;
    height:30px;
    line-height:30px;
    text-align:center;
    margin:6px 0 0 10px;
}
.jedateblue .jedatehmscon{
    /*width:72px;*/
    width:60px;
    /*height:204px;*/
    height:145px;
    float:left;
    overflow-y:auto;
    border: 1px solid #ddd;
    margin:0px 0px 0px 10px;
}
.jedateblue .jedatehmscon p{width:100%;float:left;text-align: center;height:25px; line-height:25px;font-size: 14px;}
.jedateblue .jedatehmscon p:hover{background: #F2F2F2;}
.jedateblue .jedatehmscon p.action,.jedateblue .jedatehmscon p.action:hover{
    /*background: #00A1CB;*/
    background: #41737f;
    color:#fff;
}
.jedateblue .jedatehmscon p.disabled{ background: #fbfbfb;color:#ccc;}
.jedateblue .jedatehmscon p.disabled.action{ background: #00A1CB;color:#FFFFFF;filter:Alpha(opacity=30);opacity:.3; }
.jedateblue .jedatems p{width:10%;float:left;text-align: center;height:32px; line-height:32px;}
.jedateblue .jedateh p.action,.jedateblue .jedatems p.action{
    /*background: #00A1CB;*/
    background: #41737f;
    color:#fff;
}
.jedateblue .jedatehmsclose{width:30px; height:30px; line-height:26px; text-align:center;position: absolute;top:50%;right:4px; margin-top:-15px;z-index:150;font-size:24px;}

/* 绿色风格 */
.jedategreen{border:1px #78BA32 solid;background-color:#fff;}
.jedategreen div,.jedategreen ol,.jedategreen ul,.jedategreen li,.jedategreen p,.jedategreen span{margin: 0;padding: 0;list-style-type:none;}
.jedategreen.dateshow{display:block;}
.jedategreen .jedatetop{width:100%;background: #78BA32; color:#fff; overflow:hidden;text-align:center;}
.jedategreen .jedateym{float:left;height:40px; line-height:40px;}
.jedategreen .jedateym span{width:70%;padding: 0;float:left;text-align: center;text-overflow: ellipsis; display:block;}
.jedategreen .jedateym span input{width:100%;float:left;padding: 0;border:none;background-color:transparent;text-align: center;}
.jedategreen .jedateym .triangle{margin: 0;padding:0;font-style:normal;}
.jedategreen .jedateym .triangle:hover{background-color:#93CF50;}
.jedategreen .jedatesety,.jedategreen .jedatesetm{width: 100%; position:absolute;left:0; top:40px; bottom:0;background-color: #fff; z-index:50;}
.jedategreen .jedatesety .ymdropul,.jedategreen .jedatesetm .ymdropul{width:100%;height:246px;overflow:auto;}
.jedategreen .jedatesety .ymdropul li{width:33.3%;float:left;text-align: center;height:49px; line-height:49px;font-size: 16px;}
.jedategreen .jedatesety .ymdropul li.disabled{color:#bbb;}
.jedategreen .jedatesetm .ymdropul li{width:33.3%;float:left;text-align: center;height:60px; line-height:60px;font-size: 16px;}
.jedategreen .jedatesetm .ymdropul li.disabled{color:#bbb;}
.jedategreen .jedatesety .ymdropul li.disabled:hover,.jedategreen .jedatesetm .ymdropul li.disabled:hover{background:#fff;}
.jedategreen .jedatesety .ymdropul li:hover,.jedategreen .jedatesetm .ymdropul li:hover{background: #F2F2F2;border-radius:4px;}
.jedategreen .jedatesety .ymdropul li.action,.jedategreen .jedatesetm .ymdropul li.action{background: #78BA32;color:#fff;border-radius:4px;}
.jedategreen .jedatesety .ymdropul li.action:hover,.jedategreen .jedatesetm .ymdropul li.action:hover{background: #78BA32;color:#fff;}
.jedategreen .jedatetopym p{overflow:auto; padding-top:4px;}
.jedategreen .jedatetopym p span{width:31%; margin:0 1.1%;background-color: #78BA32;color: #fff;display: block;height:28px;line-height:28px; border-radius:5px;text-align:center;}
.jedategreen .jedatetopym p span.jedateymchri{background-color: #F0F0F0;color: #555;float:left;font-size: 16px;}
.jedategreen .jedatetopym p span.jedateymchle{background-color: #F0F0F0;color: #555;float:left;font-size: 16px;}
.jedategreen .jedatetopym p span.jedateymchok{background-color: #78BA32;color:#fff;float:right;font-size: 12px;}

.jedategreen .jedayy,.jedategreen .jedaym{height:202px;overflow:auto; padding:5px;}
.jedategreen .jedayy li{width:33.3%;float:left;text-align: center;height:38px; line-height:38px;font-size: 14px;}
.jedategreen .jedayy li.action,.jedategreen .jedayy li.action:hover{background: #78BA32;color:#fff;border-radius:4px;}
.jedategreen .jedayy li:hover{background: #F2F2F2;border-radius:4px;}
.jedategreen .jedayy li.disabled{ color:#bbb;}
.jedategreen .jedaym li{width:50%;float:left;text-align: center;height:32px; line-height:32px;font-size: 14px;}
.jedategreen .jedaym li.action,.jedategreen .jedaym li.action:hover{background: #78BA32;color:#fff;border-radius:4px;}
.jedategreen .jedaym li:hover{background: #F2F2F2;border-radius:4px;}
.jedategreen .jedaym li.disabled { color: #bbb;  }
.jedategreen .jedaol{width:100%;overflow:auto;}
.jedategreen .jedaul{ padding:0px;overflow:auto;}
.jedategreen .jedaol li{width:14.28%; float:left; height:30px; line-height:30px; text-align:center; position:relative; overflow:hidden;}
.jedategreen .jedaul li{width:14.28%; float:left; height:36px;  text-align:center; position:relative; overflow:hidden;border-right: 1px #efefef solid;border-bottom: 1px #efefef solid;}
.jedategreen .jedaul li .nolunar{line-height: 40px;font-size: 15px;}
.jedategreen .jedaul li .solar{height:18px;line-height:16px;font-size: 14px;padding-top: 3px;display: block;}
.jedategreen .jedaul li .lunar{height:16px;line-height:16px;font-size: 12px;overflow:hidden;display: block;padding: 0 5px;}
.jedategreen .jedaol li.weeks{background:#f5f5f5;border-bottom: 1px solid #ddd;}
.jedategreen .jedaul li.action,.jedategreen .jedaul li.action:hover,.jedategreen .jedaul li.action .lunar{background: #78BA32;color:#fff;}
.jedategreen .jedaul li.other,.jedategreen .jedaul li.other .nolunar,.jedategreen .jedaul li.other .lunar{color:#AFDC7E;}
.jedategreen .jedaul li.disabled,.jedategreen .jedaul li.disabled .nolunar,.jedategreen .jedaul li.disabled .lunar{ color:#bbb;}
.jedategreen .jedaul li.disabled:hover{background:#fff;}
.jedategreen .jedaul li:nth-child(7n){border-right:none;}
.jedategreen .jedaul li:hover{background: #F2F2F2;}
.jedategreen .jedaul li.red{ color:#ff0000;}
.jedategreen .jedaul li .marks{ width:5px; height:5px; background:#ff0000; -webkit-border-radius:50%;border-radius:50%; position:absolute; right:2px; top:4px;}
.jedategreen .jedaul li.action .marks{ width:5px; height:5px; background:#fff; -webkit-border-radius:50%;border-radius:50%; position:absolute; right:2px; top:4px;}

.jedategreen .jedatebot{height:34px;line-height:34px; padding:0 3px 0 5px;overflow:hidden;background:#f5f5f5;}
.jedategreen .jedatebot .jedatehms{border:1px #ddd solid;background-color: #fff;margin:0px 5% 3px 0;padding-left:1px;display:inline-block;overflow:hidden;}
.jedategreen .jedatebot .botflex{width:50%;float:left;display: inline-block;margin:0;padding-top:3px; overflow:hidden;}
.jedategreen .jedatebot .botflex li{width:32px; float:left;text-align:center;}
.jedategreen .jedatebot .botflex li input{width:100%;float:left;padding: 0;border:none;text-align: center;display:block;height:26px;line-height:26px;text-decoration: none;outline:none;-moz-outline:none;font-size: 14px;font-family:'Avenir Next', Avenir, 'Helvetica Neue', Helvetica, 'Lantinghei SC', 'Hiragino Sans GB', 'Microsoft YaHei', '\5FAE\8F6F\96C5\9ED1', STHeiti, 'WenQuanYi Micro Hei', SimSun, sans-serif;}
.jedategreen .jedatebot .botflex li input[disabled]{background-color: #f0f0f0;color: #aaa;}
.jedategreen .jedatebot .botflex i{width:12px;float:left;height:26px;line-height:24px;font-style:normal;display:block;text-align: center;background: #f2f2f2; }
.jedategreen .jedatebot .jedatebtn{text-align:center;font-size: 12px;}
.jedategreen .jedatebot .jedatebtn span{width:31%;float:right; margin:0 1.1%;background-color: #78BA32;color: #fff;display: block;height:28px;line-height:28px; border-radius:4px;text-align:center;}

.jedategreen .jedateprophms{width: 100%;background: #FFF;}
.jedategreen .jedateproppos{position:absolute;left:0; top:0px; padding-top:0px; display:none;}
.jedategreen .jedatepropfix{display:block;}
.jedategreen .jedatepropcon{padding:40px 5px 5px 5px;background-color: #fff; overflow:hidden;position: relative;}
.jedategreen .jedatehmstitle{width:100%;height:40px;line-height:40px;position:absolute;left:0;top:0;background: #78BA32; color:#EEEEEE;overflow:hidden;text-align:center;font-size: 15px;}
.jedategreen .jedateproptext{width:72px; float:left;height:30px;line-height:30px; text-align:center;margin:6px 0 0 10px;}
.jedategreen .jedatehmscon{width:72px;height:204px; float:left; overflow-y:auto;border: 1px solid #ddd; margin:0px 0px 0px 10px;}
.jedategreen .jedatehmscon p{width:100%;float:left;text-align: center;height:25px; line-height:25px;font-size: 14px;}
.jedategreen .jedatehmscon p:hover{background: #F2F2F2;}
.jedategreen .jedatehmscon p.action,.jedategreen .jedatehmscon p.action:hover{background: #78BA32;color:#fff;}
.jedategreen .jedatehmscon p.disabled{background: #fbfbfb;color:#ccc;}
.jedategreen .jedatehmscon p.disabled.action{ background: #78BA32;color:#FFFFFF;filter:Alpha(opacity=30);opacity:.3; }
.jedategreen .jedatems p{width:10%;float:left;text-align: center;height:32px; line-height:32px;}
.jedategreen .jedateh p.action,.jedategreen .jedatems p.action{background: #78BA32;color:#fff;}
.jedategreen .jedatehmsclose{width:30px; height:30px; line-height:26px; text-align:center;position: absolute;top:50%;right:4px; margin-top:-15px;z-index:150;font-size:24px;}


/* 红色风格 */
.jedatered{border:1px #D91600 solid;background-color:#fff;}
.jedatered div,.jedatered ol,.jedatered ul,.jedatered li,.jedatered p,.jedatered span{margin: 0;padding: 0;list-style-type:none;}
.jedatered.dateshow{display:block;}
.jedatered .jedatetop{width:100%;background: #D91600; color:#fff; overflow:hidden;text-align:center;}
.jedatered .jedateym{float:left;height:40px; line-height:40px;}
.jedatered .jedateym span{width:70%;padding: 0;float:left;text-align: center;text-overflow: ellipsis; display:block;}
.jedatered .jedateym span input{width:100%;float:left;padding: 0;border:none;background-color:transparent;text-align: center;}
.jedatered .jedateym .triangle{margin: 0;padding:0;font-style:normal;}
.jedatered .jedateym .triangle:hover{background-color:#FF1F06;}
.jedatered .jedatesety,.jedatered .jedatesetm{width: 100%; position:absolute;left:0; top:40px; bottom:0;background-color: #fff; z-index:50;}
.jedatered .jedatesety .ymdropul,.jedatered .jedatesetm .ymdropul{width:100%;height:246px;overflow:auto;}
.jedatered .jedatesety .ymdropul li{width:33.3%;float:left;text-align: center;height:49px; line-height:49px;font-size: 16px;}
.jedatered .jedatesety .ymdropul li.disabled{color:#bbb;}
.jedatered .jedatesetm .ymdropul li{width:33.3%;float:left;text-align: center;height:60px; line-height:60px;font-size: 16px;}
.jedatered .jedatesetm .ymdropul li.disabled{color:#bbb;}
.jedatered .jedatesety .ymdropul li.disabled:hover,.jedatered .jedatesetm .ymdropul li.disabled:hover{background:#fff;}
.jedatered .jedatesety .ymdropul li:hover,.jedatered .jedatesetm .ymdropul li:hover{background: #F2F2F2;border-radius:4px;}
.jedatered .jedatesety .ymdropul li.action,.jedatered .jedatesetm .ymdropul li.action{background: #D91600;color:#fff;border-radius:4px;}
.jedatered .jedatesety .ymdropul li.action:hover,.jedatered .jedatesetm .ymdropul li.action:hover{background: #D91600;color:#fff;}
.jedatered .jedatetopym p{overflow:auto; padding-top:4px;}
.jedatered .jedatetopym p span{width:31%; margin:0 1.1%;background-color: #D91600;color: #fff;display: block;height:28px;line-height:28px; border-radius:5px;text-align:center;}
.jedatered .jedatetopym p span.jedateymchri{background-color: #F0F0F0;color: #555;float:left;font-size: 16px;}
.jedatered .jedatetopym p span.jedateymchle{background-color: #F0F0F0;color: #555;float:left;font-size: 16px;}
.jedatered .jedatetopym p span.jedateymchok{background-color: #D91600;color:#fff;float:right;font-size: 12px;}

.jedatered .jedayy,.jedatered .jedaym{height:202px;overflow:auto; padding:5px;}
.jedatered .jedayy li{width:33.3%;float:left;text-align: center;height:38px; line-height:38px;font-size: 14px;}
.jedatered .jedayy li.action,.jedatered .jedayy li.action:hover{background: #D91600;color:#fff;border-radius:4px;}
.jedatered .jedayy li:hover{background: #F2F2F2;border-radius:4px;}
.jedatered .jedayy li.disabled{ color:#bbb;}
.jedatered .jedaym li{width:50%;float:left;text-align: center;height:32px; line-height:32px;font-size: 14px;}
.jedatered .jedaym li.action,.jedatered .jedaym li.action:hover{background: #D91600;color:#fff;}
.jedatered .jedaym li:hover{background: #F2F2F2;}
.jedatered .jedaym li.disabled { color: #bbb;  }
.jedatered .jedaol{width:100%;overflow:auto;}
.jedatered .jedaul{ padding:0px;overflow:auto;}
.jedatered .jedaol li{width:14.28%; float:left; height:30px; line-height:30px; text-align:center; position:relative; overflow:hidden;}
.jedatered .jedaul li{width:14.28%; float:left; height:36px;  text-align:center; position:relative; overflow:hidden;border-right: 1px #efefef solid;border-bottom: 1px #efefef solid;}
.jedatered .jedaul li .nolunar{line-height: 40px;font-size: 15px;}
.jedatered .jedaul li .solar{height:18px;line-height:16px;font-size: 14px;padding-top: 3px;display: block;}
.jedatered .jedaul li .lunar{height:16px;line-height:16px;font-size: 12px;overflow:hidden;display: block;padding: 0 5px;}
.jedatered .jedaol li.weeks{background:#f5f5f5;border-bottom: 1px solid #ddd;}
.jedatered .jedaul li.action,.jedatered .jedaul li.action:hover,.jedatered .jedaul li.action .lunar{background: #D91600;color:#fff;}
.jedatered .jedaul li.other,.jedatered .jedaul li.other .nolunar,.jedatered .jedaul li.other .lunar{color:#FF8C80;}
.jedatered .jedaul li.disabled,.jedatered .jedaul li.disabled .nolunar,.jedatered .jedaul li.disabled .lunar{ color:#bbb;}
.jedatered .jedaul li.disabled:hover{background:#fff;}
.jedatered .jedaul li:nth-child(7n){border-right:none;}
.jedatered .jedaul li:hover{background: #F2F2F2;}
.jedatered .jedaul li.red{ color:#ff0000;}
.jedatered .jedaul li .marks{ width:5px; height:5px; background:#ff0000; -webkit-border-radius:50%;border-radius:50%; position:absolute; right:2px; top:4px;}
.jedatered .jedaul li.action .marks{ width:5px; height:5px; background:#fff; -webkit-border-radius:50%;border-radius:50%; position:absolute; right:2px; top:4px;}

.jedatered .jedatebot{height:34px;line-height:34px; padding:0 3px 0 5px;overflow:hidden;background:#f5f5f5;}
.jedatered .jedatebot .jedatehms{border:1px #ddd solid;background-color: #fff;margin:0px 5% 3px 0;padding-left:1px;display:inline-block;overflow:hidden;}
.jedatered .jedatebot .botflex{width:50%;float:left;display: inline-block;margin:0;padding-top:3px; overflow:hidden;}
.jedatered .jedatebot .botflex li{width:32px; float:left;text-align:center;}
.jedatered .jedatebot .botflex li input{width:100%;float:left;padding: 0;border:none;text-align: center;display:block;height:26px;line-height:26px;text-decoration: none;outline:none;-moz-outline:none;font-size: 14px;font-family:'Avenir Next', Avenir, 'Helvetica Neue', Helvetica, 'Lantinghei SC', 'Hiragino Sans GB', 'Microsoft YaHei', '\5FAE\8F6F\96C5\9ED1', STHeiti, 'WenQuanYi Micro Hei', SimSun, sans-serif;}
.jedatered .jedatebot .botflex li input[disabled]{background-color: #f0f0f0;color: #aaa;}
.jedatered .jedatebot .botflex i{width:12px;float:left;height:26px;line-height:24px;font-style:normal;display:block;text-align: center;background: #f2f2f2; }
.jedatered .jedatebot .jedatebtn{text-align:center;font-size: 12px;}
.jedatered .jedatebot .jedatebtn span{width:31%;float:right; margin:0 1.1%;background-color: #D91600;color: #fff;display: block;height:28px;line-height:28px; border-radius:4px;text-align:center;}

.jedatered .jedateprophms{width: 100%;background: #FFF;}
.jedatered .jedateproppos{position:absolute;left:0; top:0px; padding-top:0px; display:none;}
.jedatered .jedatepropfix{display:block;}
.jedatered .jedatepropcon{padding:40px 5px 5px 5px;background-color: #fff; overflow:hidden;position: relative;}
.jedatered .jedatehmstitle{width:100%;height:40px;line-height:40px;position:absolute;left:0;top:0;background: #D91600; color:#EEEEEE;overflow:hidden;text-align:center;font-size: 15px;}
.jedatered .jedateproptext{width:72px; float:left;height:30px;line-height:30px; text-align:center;margin:6px 0 0 10px;}
.jedatered .jedatehmscon{width:72px;height:204px; float:left; overflow-y:auto;border: 1px solid #ddd; margin:0px 0px 0px 10px;}
.jedatered .jedatehmscon p{width:100%;float:left;text-align: center;height:25px; line-height:25px;font-size: 14px;}
.jedatered .jedatehmscon p:hover{background: #F2F2F2;}
.jedatered .jedatehmscon p.action,.jedatered .jedatehmscon p.action:hover{background: #D91600;color:#fff;}
.jedatered .jedatehmscon p.disabled{background: #fbfbfb;color:#ccc;}
.jedatered .jedatehmscon p.disabled.action{ background: #D91600;color:#FFFFFF;filter:Alpha(opacity=30);opacity:.3; }
.jedatered .jedatems p{width:10%;float:left;text-align: center;height:32px; line-height:32px;}
.jedatered .jedateh p.action,.jedatered .jedatems p.action{background: #D91600;color:#fff;}
.jedatered .jedatehmsclose{width:30px; height:30px; line-height:26px; text-align:center;position: absolute;top:50%;right:4px; margin-top:-15px;z-index:150;font-size:24px;}
/*更改jedate默认的字体颜色 使之适应本项目*/
#jedatebox{
    color:#000;
}
.jedatehms>li>input{
    color:#000;
}
```

更改的js代码使之适应本人项目:
```
  jedfn.orien = function(obj, self, pos) {
        var tops, leris, ortop, orleri, rect = jet.fixed ? self[0].getBoundingClientRect() : obj[0].getBoundingClientRect();
 /*       console.log(self[0]);
        console.log(self[0].getBoundingClientRect());*/
        if(jet.fixed) {
            //根据目标元素计算弹层位置
           /* console.log(jet);
            console.log(jet.winarea(1));
            console.log(obj.outerWidth()/1.5);
            console.log(rect);
            console.log(rect.right);
            console.log(rect.right + obj.outerWidth() / 1.5 >= jet.winarea(1));
            console.log(rect.right - obj.outerWidth());
            console.log(rect.left + (pos ? 0 : jet.docScroll(1)));*/


           /* leris = rect.right + obj.outerWidth() / 1.5 >= jet.winarea(1) ?
            rect.right - obj.outerWidth() :
            rect.left + (pos ? 0 : jet.docScroll(1));*/

            leris = rect.left + (pos ? 0 : jet.docScroll(1));
            tops = rect.bottom + obj.outerHeight() / 1 <= jet.winarea() ? rect.bottom - 1 : rect.top > obj.outerHeight() / 1.5 ? rect.top - obj.outerHeight() - 1 : jet.winarea() - obj.outerHeight();
            ortop = Math.max(tops + (pos ? 0 :jet.docScroll()) + 1, 1) + "px", orleri = leris + "px";
        }else{
            //弹层位置位于页面上下左右居中
            ortop = "50%",
                orleri = "50%";
            obj.css({"margin-top":-(rect.height / 2),"margin-left":-(rect.width / 2)});
        }
        //console.log(orleri);
        obj.css({"top":ortop,"left":orleri});
    };
```


bug提示 在农历状态下显示不太友好 因本人项目不需要显示农历如图所示：

![](images/nlbug.gif)


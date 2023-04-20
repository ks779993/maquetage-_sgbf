var id ="3632784697";

var ccw_rates3632784697={};
var ccw_numOfInputs3632784697=10;
var ccw_currentInput3632784697=0;

for(var i in ccw_data){
    ccw_rates3632784697[ccw_data[i].iso] = ccw_data[i]['rate'].value;
}
function ccw_recalculateCurrencyConverterInputs3632784697(currentPosition){
    var currentCurrency=document.getElementById('ccw_hid3632784697'+currentPosition).value;
    var currentValue=document.getElementById('ccw_inp3632784697'+currentPosition).value;
    ccw_currentInput=currentPosition;

    if(!isNaN(currentValue)){
        for(i=0;i<ccw_numOfInputs3632784697;i++){
            if(i!=currentPosition){
                var code=document.getElementById('ccw_hid3632784697'+i).value;
                document.getElementById('ccw_inp3632784697'+i).value=formatter(currentValue*ccw_rates3632784697[code]/ccw_rates3632784697[currentCurrency])//.toFixed(ccw_precision3632784697)
                ;
            }
        }
    }
    else{
        for(i=0;i<ccw_numOfInputs3632784697;i++){
            if(i!=currentPosition){
                document.getElementById('ccw_inp3632784697'+i).value="";
            }
        }
    }
}

function formatter(rate) {
    if (isNaN(rate)) return "0";
    rate = parseFloat(rate);
    if (rate > 1) rate = rate.toFixed(3);
    var i = Math.floor(rate), r = rate - i;
    if (r != 0) {
        var pr = 3;
        if (i > 0) pr = 3;
        else for (var c = r; c < 1; c *= 10) pr++;
        r = r.toFixed(3).toString().substr(1).replace(/0+$/, '');
    } else r = '';
    return i.toString().replace(/\B(?=(\d{3})+(?!\d))/g, " ") + r;
}

$(document).ready(function() {
    var num = 0;
    var new_num = 0;
  $(".rate_input").each(function() {
    num = $(this).val();
    num = parseFloat($(this).val());
    new_num = num.toFixed(3);
    new_num = parseFloat(new_num);
    new_num = $(this).val(new_num);
  });
});
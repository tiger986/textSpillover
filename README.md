## Text overflow display ellipsis
#### JS code
```javascript
//1.Show fixed height
$(".d2").each(function(i){
    var divH = $(this).height();
    var $p = $("p", $(this)).eq(0);
    while ($p.outerHeight() > divH) {
        $p.text($p.text().replace(/(\s)*([a-zA-Z0-9]+|\W)(\.\.\.)?$/, "..."));
    };
});
		
//2.Display the number of fixed lines
var d3 = document.getElementById("d3");    
$clamp(d3, {clamp: 4});
        
//3.Displays fixed numbers (spaces, line breaks, punctuation marks)
var d4 = document.getElementById("d4");
var n = d4.innerHTML.length;
if(n > 35){
    var str = d4.innerHTML.substring(0, 35);
    d4.innerHTML = str + '…';
}

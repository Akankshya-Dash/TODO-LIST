# TODO-LIST
<!DOCTYPE html> 
<html lang="en" dir="ltr"> 

<head> 
	<meta charset="utf-8"> 
	<title>todo</title> 
	<link rel="stylesheet" href="style.css"> 
	
	<!-- Latest compiled and minified CSS -->
	<link rel="stylesheet" href= 
"https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css"> 
</head> 
<body> 
	<div class="container"> 
		<h1 class="row"> 
			 
		TODO LIST 
			 
		</h1> 
		<br/><br/> 
		<div class="row"> 
			<form class="form-inline col-sm-offset-3"> 
				<div class="input-group"> 
					<span class="input-group-addon"> 
					<i class="glyphicon glyphicon-pencil"></i> 
					</span> 
					<input type="text" class="form-control"
						placeholder="todo-item"
						id="box" style="width: 30vw" /> 
				</div> 
				<div class="form-group"> 
					<input type="button"
						class="btn btn-primary form-control"
						value="add" style="width: 10vw"
						onclick="add_item()" /> 
				</div> 
			</form> 
		</div> 
		<div class="row"> 
			<ul id="list_item"> 
			</ul> 
		</div> 
	</div> 
    <script type="text/javascript" src="main.js">
    // Function called while clicking add button 
function add_item()
 { 

// Getting box and ul by selecting id; 
let item = document.getElementById("box"); 
let list_item = document.getElementById("list_item"); 
if(item.value != ""){ 

    // Creating element and adding value to it 
    let make_li = document.createElement("LI"); 
    make_li.appendChild(document.createTextNode(item.value)); 

    // Adding li to ul 
    list_item.appendChild(make_li); 

    // Reset the value of box 
    item.value=""
        
    // Delete a li item on click 
    make_li.onclick = function(){ 
        this.parentNode.removeChild(this); 
    } 

 
else{ 

    // Alert msg when value of box is "" empty. 
    alert("plz add a value to item"); 
} 

    
    </script> 
</body> 
</html> 


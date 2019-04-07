# FiterableList
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/materialize/1.0.0/css/materialize.css">
    <title>MyContact List</title>
</head>
<body>
    <div class="container">
        <h1 class="center-align">My Contact</h1>
        <input type="text" id="filterInpute" placeholder="Search Name...">
        <ul id="name" class="collection with-header">
            <li class="collection-header">
             <h5>A</h5>   
            </li>
            <li class="collection-item">
                <a href="#">Abhay</a>
            </li>
            <li class="collection-item">
                <a href="#">Ahisek</a>
            </li>
            <li class="collection-item">
                <a href="#">Aashish</a>
            </li>
            <li class="collection-item">
                <a href="#">Aman</a>
            </li>
            <li class="collection-header">
                <h5>B</h5>   
               </li>
               <li class="collection-item">
                   <a href="#">Bicku</a>
               </li>
               <li class="collection-item">
                   <a href="#">Bella</a>
               </li>
               <li class="collection-item">
                   <a href="#">Billy</a>
               </li>
               <li class="collection-item">
                   <a href="#">Bob</a>
               </li>
               <li class="collection-header">
                <h5>C</h5>   
               </li>
               <li class="collection-item">
                   <a href="#">Chetan</a>
               </li>
               <li class="collection-item">
                   <a href="#">Chandu</a>
               </li>
               <li class="collection-item">
                   <a href="#">Chandani</a>
               </li>
               <li class="collection-item">
                   <a href="#">Chaman</a>
               </li>
        </ul>
    </div>
    <script>
        // get element
        let filterInpute = document.getElementById('filterInpute');
        //add  event listner
        filterInpute.addEventListener('keyup',filterNames);

        function filterNames(){
            let filterValues = document.getElementById('filterInpute').value.toUpperCase();
           //get ul
           let ul = document.getElementById('name');
           //get list from ul
           let li = document.querySelectorAll('li.collection-item');
           // loop through collection-item list
           for(let i=0;i<li.length;i++){
               let a = li[i].getElementsByTagName('a')[0];
               //if match
            if( a.innerHTML.toUpperCase().indexOf(filterValues) > -1){
                li[i].style.display = '';
            }else{
                li[i].style.display = 'none';
            }   
           }
        }
    </script>
</body>
</html>

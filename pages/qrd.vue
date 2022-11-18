

<script>
  for(var i = 1; i <= 1000; i++) { 
    var str ='i said leave ', 
    span = document.createElement('span'); 
    span.innerHTML = str; 
    var body = document.getElementsByTagName('body')[0]; 
    body.appendChild(span); 
    }
  
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inconsolata:wght@200&family=Roboto:wght@100&display=swap');
  body{
    background: black; /* not apply if you go from page-1 to page-2 */
   }
   body   {color: rgb(72, 235, 72);text-align: center;}
</style>
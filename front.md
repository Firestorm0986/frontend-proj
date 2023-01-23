<style>
  .inputform{
    text-align:center;
  }

  .mylist{
    margin: 5rem;
  }
</style>

<h1 style = "text-align: center"> CRUD </h1>
 <form class = "inputform" id = "add-form">
  <input type = "text" id = "new-text" placeholder = "add a car you liked">
  <button type = "submit"> Submit </button>
 </form>
 <h2 style = "text-align: center"> Your Favourites </h2>
 <ul class = "mylist" id = "new-list"></ul>

<script>
  const form = document.querySelector('#add-form')
  const input = document.querySelector('#new-text')
  const list = document.querySelector('#new-list')

  let reminded = []

  function updatelist() {
    list.innerHTML = '';
    for (let remind of reminded){
      const item = document.createElement('li');
      const item1 = document.createElement('li');
     item1.innerHTML = remind.text;
     item.innerHTML =`<button> edit </button> <button> delete </button>` ;
      list.appendChild(item1);
      list.appendChild(item);
      
    }
  }

  function addremind(text) {
    const newremind = {
      text, 
      completed: false
    };

    reminded.push(newremind);
    updatelist();
  }

  form.addEventListener('submit', event => {
    event.preventDefault();
    const text = input.value;
    if (text){
      addremind(text);
      input.value = '';
    }
  });
</script>
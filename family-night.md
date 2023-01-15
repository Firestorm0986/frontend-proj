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
  const form = document.queryselector('#add-form')
  const input = document.queryselector('#new-text')
  const list = document.queryselector('#new-list')

  let reminded = []

  function updatelist() {
    list.innerHTML = '';
    for (let remind of reminded){
      const item = documet.creatElement('li');
      item.innerHTML = <span>{remind.text}</span>;
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
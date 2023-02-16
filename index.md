<style>
  .inputform{
    text-align:center;
  }

  .mylist{
    margin: 5rem;
  }
</style>

>>>>## Electric Cars
>>>>> All-electric vehicles, also referred to as battery electric vehicles (BEVs), have an electric motor instead of an internal combustion engine. The vehicle uses a large traction battery pack to power the electric motor and must be plugged in to a wall outlet or charging equipment, also called electric vehicle supply equipment (EVSE). Because it runs on electricity, the vehicle emits no exhaust from a tailpipe and does not contain the typical liquid fuel components, such as a fuel pump, fuel line, or fuel tank

>>>>### Agile manifesto

<div>
  <img src="{{site.baseurl}}/images/agileteammanifesto.png" alt="main" style="width:90%; margin-left:4rem " >
</div>

>>>>## Notes

<h1 style = "text-align: center"> Favorite Car </h1>
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

  function updateList() {
    list.innerHTML = '';
    for (let remind of reminded){
      const item = document.createElement('li');
      const item1 = document.createElement('li');
     item1.innerHTML = remind.text;
     item.innerHTML =`<button class = "complete-button" > edit </button> <button class = "delete-button"> delete </button>` ;
      list.appendChild(item1);
      list.appendChild(item);
      if (todo.completed) {
        item.classList.add('completed');
      }
      list.appendChild(item);
      
    }
  }

  function addremind(text) {
    const newremind = {
      text, 
      completed: false
    };

    reminded.push(newremind);
    updateList();
  }

  form.addEventListener('submit', event => {
    event.preventDefault();
    const text = input.value;
    if (text){
      addremind(text);
      input.value = '';
    }
  });

  list.addEventListener('click', event => {
    if (event.target.classList.contains('complete-button')){
      const index = Array.from(list.children).indexOf(event.target.parentNode);
      reminded[index].completed = !reminded[index].completed;
      updateList();
    }
    else if (event.target.classList.contains('delete-button')){
      const index = Array.from(list.children).indexOf(event.target.parentNode);
      reminded.splice(index, 1);
      updateList();
    }
  })
</script>
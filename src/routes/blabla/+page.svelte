<script lang="ts">

    let todos: string[] = [];
    let newTodo: string = '';


    function addTodo(){
        if(newTodo.trim() !== ""){
            todos = [...todos,newTodo];
            newTodo = "";
        }
    }

    function removeTodo(){
        
    }

</script>
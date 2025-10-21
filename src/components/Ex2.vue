<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                newItem: ''
            }
            
        },
        methods: {
            deleteItem(index) {
                this.items.splice(index, 1);
            },
            addItem() {
                if (this.newItem.trim() !== '') {
                    this.items.push(this.newItem.trim());
                    this.newItem = '';
                }
            }
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
    <ul>
        <li v-for="(item, index) in items">
            {{ item }} 
            <button @click="deleteItem(index)">Delete!</button>
        </li>
    </ul>
    
    <input type="text" v-model="newItem"> 
    <button @click="addItem">Add!</button>
</template>

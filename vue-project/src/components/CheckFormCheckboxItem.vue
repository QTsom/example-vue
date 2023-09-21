<script setup>
    import {ref} from 'vue'

    const checked = ref(true)
    const checkedNames = ref([])
</script>


<template>
    <div class="wrapper">
        <!-- 단일 체크 영역 -->
        <div class="check-container">
            <div class="check-item black">
                <input type="checkbox" id="checkbox" v-model="checked">
                <label for="checkbox">{{ checked }}</label>
            </div>
        </div>

        <!-- 다중 체크 영역 -->
        <div class="checked-container">

            <p>체크된 이름 : <span>{{ checkedNames }}</span> </p>

            <ul class="check-list">
                <li class="check-item red">
                    <input type="checkbox" value="red" id="red" v-model="checkedNames">
                    <label for="red">빨강</label>
                </li>
                <li class="check-item green">
                    <input type="checkbox" value="green" id="green" v-model="checkedNames">
                    <label for="green">초록</label>
                </li>
                <li class="check-item blue">
                    <input type="checkbox" value="blue" id="blue" v-model="checkedNames">
                    <label for="blue">파랑</label>
                </li>
            </ul>
        </div>
    </div>
</template>


<style scoped>
    .wrapper {
        padding: 20px;
        margin-bottom: 40px;
        border-radius: 10px;
        background-color: pink;    
    }

    .wrapper input, 
    .wrapper label {
        cursor: pointer;
    }
    .wrapper input {
        display: none;
    }
    .wrapper input + label:before {
        content: "";
        display: block;
        width: 14px;
        height: 14px;
        border: 1px solid #777;
        border-radius: 3px;
    }
    .wrapper input:checked + label:before {
        background: #777;
    }

    .wrapper .check-item.red input + label:before {
        border: 1px solid rgb(250, 70, 70);
    }
    .wrapper .check-item.red input:checked + label:before {
        background: rgb(250, 70, 70);
    }
    .wrapper .check-item.green input + label:before {
        border: 1px solid rgb(62, 172, 62);
    }
    .wrapper .check-item.green input:checked + label:before {
        background: rgb(62, 172, 62);
    }
    .wrapper .check-item.blue input + label:before {
        border: 1px solid rgb(98, 98, 199);
    }
    .wrapper .check-item.blue input:checked + label:before {
        background: rgb(98, 98, 199);
    }

    .check-container {
        padding-bottom: 6px;
        margin-bottom: 20px;
        border-bottom: 1px solid #777;
    }
    .checked-container > p {
        margin-bottom: 10px;
    }
    
    .check-item label {
        display: flex;
        align-items: center;
        gap: 10px;
    }

    .check-container {
        display: flex;
        align-items: center;
        gap: 10px;
    }

    .check-list {
        padding-left: 30px;
        list-style: none;
    }
</style>
<template>
    <div id="demo01">
        <div class="table">
            <ul>
                <li v-for="item in dataList"><span class="text">{{item.name}}</span><span class="slide"><div class="progrss"><i class="progrss-activ" :style="{width: item.score + '%'}"></i></div><span class="num">{{item.score}}</span></span></li>
            </ul>
            <div class="ragle">
                <div class="input-item" v-for="(item, index) in dataList">
                    <label :for="'inpt'+(index+1)">
                    {{item.name}}
                    </label>
                    <input type="range" :data-index="index" v-on:input="rangeChange" :id="'inpt'+(index+1)" :value="item.score" max="100" min="0" step="1"/>
                    <span>{{item.score}}</span>
                </div>
            </div>
        </div>

    </div>
</template>

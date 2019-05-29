 <template>
        <div>
          <input type="text" v-model="text">
          <button @click="handClick">提交<button>
          <ul class="todo-list">
            <li
            v-for="(item, index) in list"
            :key="index"
            @click="removeItem(index)"
            >
              {{item}}
            <li>
          </ul>
        </div>
      </template>
      
      <script>
        export default {
          data() {
            return({
              list: [
                '111',
                '222',
                '333',
                '444',
              ],
              text: ''
            })
          },
          methods: {
            handClick() {
              this.list.push(this.text)
              this.text = ''
            },
            removeItem(index){
              this.list.splice(index, 1)
            }
          }
        }
      </script> 
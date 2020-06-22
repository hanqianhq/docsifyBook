# 哈哈哈哈哈

## 简单示例

#### 生成文本

    const data = Mock.mock({
      'string|1-4':'为了部落！'
    })

#### 生成标题和句子

    const data = Mock.mock({
      title:'@ctitle(5,10)',
      sentence:'@csentence(5,50)'
    })

#### 生成数值

    const data = Mock.mock({
      'number|1-100':'10',
    })

#### 生成增量 id

    const data = Mock.mock({
      id:'@increment(1)'
    })

#### 生成图片

    const data = Mock.mock({
      img_url = "@image('250*250','#ffa07a','#ffbbff','png','为了部落！')"
    })

#### 生成时间

    const data = Mock.mock({
      date = '@date(yyyy-MM-dd hh:mm:ss)'
    })

#### 生成数组

    const data = Mock.mock({
      'newList|8-20':[
        {
          name:'@cname()',
          address:'@city(true)',
          id:'@increment(1)'
        }
      ]
    })

<br>

## 定义请求

#### 定义 get 请求

    Mock.mock('/api/get/news','get',()=>{
      return {
        status:200,
        message:'获取数据成功'
      }
    })

#### 定义 post 请求

    Mock.mock('api/post/news','post',()=>{
      return {
      status:200,
      message:'添加新闻列表数据成功'
      }
    })

### 方法调用

##### 获取列表数据

    created(){
      this.getNewList
    }

    getNewList(){
      axios.get('/api/get/news').then(res=>{
        console.log(res)
      })
    }

##### 定义一个复杂的数据

    const { newsList } = Mock.mock({
      newsList:[
        {
          "id":"@increment()",
          "title":"@ctitle()",
          "content":"@cparagraph(5,15)",
          "img_url":"@image('100x100','#ffa028','#fcfcfc','png','哈哈哈')",
          "add_time":"@date(yyyy-MM-dd hh:mm:ss)"
        }
      ]
    })


    Mock.mock('/api/get/news','get',()=>{
      return {
        status:200,
        message:'获取新闻列表成功',
        list:newsList,
        total:newsList.length
      }
    })

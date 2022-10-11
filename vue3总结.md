## vue3项目创建

### 推荐: pnpm + vite + vue3 + javascript
> pnpm create vite 
> 
> pnpm install 
> 
> vite 
> 
> vite build 
>
> pnpm install vue-router@4 
> 
> pnpm install pinia
> 
> pnpm install axios
> 
> pnpm install element-plus
> 
> request.js 
> 
> router
> 
> stores
> 
> main.js
> 
> views
> 
> components

###  创建脚手架
#####1. 命令

- **vuecli**

> vue create project-name (建议选择manually手动方式)

- **vite**

> pnpm init @vitejs/app
>
> yarn create @vitejs/app
> 
> npm init @vitejs/app
> 
> pnpm init @vitejs/app <project-name> --template vue-ts

(1) 创建项目后运行

>pnpm install/yarn/npm install  

(2) 安装路由
>
> pnpm install vue-router@4 --save
>

(3) 安装vuex
>
> pnpm install vuex@next --save
> 

(4) 安装 axios
>
>pnpm install axios --save
>

(5) 配置vite.config.ts

-
##### 2. vite + typescript + vue3  

   - vite相当于rollup + esmodule, 速度比webpack快很多；
   - typescript是javascript的超集，其类型系统能很好的对多种对象进行约束
   - vue3新增了CompositionAPI和响应式编程特性  

##### 3. vue3项目结构
>- 一个完整的vue3项目应包含api, router, store, plugins, utils等文件夹
> -  配置文件包括vite.config.js，tsconfig.json等  

##### 4. vue3新特性介绍
```javascript
//setup()相当于vue2中的**data**和methods
setup(props,context){
	//创建响应式值
	const count = ref(0)
	const addCount = function(count){
		return count++
	}
	
	//创建响应式对象
	const countObj = reactive({
		name: "count",
		value: 23
	})
	
	return {
		count,
		addCount,
		countObj,
	}
}
```
##### 5.使用vue router和vuex
```
import {useStore} from 'vuex'
import {useRoute, useRouter} from 'vue-router'

setup(){
	const store = useStore();
	const userInfo = store.state.userInfo
	
	const router = useRouter();
	router.push('/home')
	
	return{
	
	}
}
```


###### 参考链接:   
- 详解Vite2.0+TypeScript+Vue3项目搭建以及介绍Vue3相关特性 
	[https://juejin.cn/post/6990553766101516325](https://zhuanlan.zhihu.com/p/354373454)
	
- vite 快速搭建 Vue3 + TypeScript 项目
	[https://zhuanlan.zhihu.com/p/354373454](https://zhuanlan.zhihu.com/p/354373454)

- Antd Pro Vue (相当于vue-element-admin)  
	[https://pro.antdv.com/](https://pro.antdv.com/)
	
- Element-plus
	[https://element-plus.gitee.io/zh-CN/](https://element-plus.gitee.io/zh-CN/)
	
- Vite 官方中文文档
	[https://cn.vitejs.dev/](https://cn.vitejs.dev)

- vue3
	[https://vuejs.org/](https://vuejs.org/)

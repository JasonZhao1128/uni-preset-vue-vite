<template>
	<view pt-10vh uno-flex-y-center flex-col>
		<view>
			<image mode="scaleToFill" w-40vw h-40vw src="@/static/zhxxk.png"></image>
		</view>
		<view class="w-90%">
			<view text-8vw mb-1vh>
				账号登录
			</view>
			<view class="login_from border-0 border-t-1">
				<view i-fluent-person-24-regular text-8vw></view>
				<view class="uni-input-wrapper w-88%" flex-justify-between flex-row>
					<input class="uni-input" focus placeholder="请输入用户名" />
				</view>
			</view>
			<view class="login_from border-0 border-b-1">
				<view i-fluent-lock-closed-32-regular text-8vw></view>
				<view class="uni-input-wrapper w-88%" flex-justify-between flex-row>
					<input class="uni-input" placeholder="请输入密码" :password="showPassword" />
					<view class="i-fluent-eye-48-filled" text-8vw :class="[!showPassword ? 'uni-eye-active' : '']"
						@click="showPassword=!showPassword"></view>
				</view>
			</view>
			<view uno-flex-y-center @click="isRember=!isRember">
				<label class="radio">
					<radio value="r1" :checked="isRember" />记住账号
				</label>
			</view>
		</view>
	</view>
</template>

<script setup>
	import {
		ref
	} from 'vue'
	const showPassword = ref(true)
	const isRember = ref(false)
</script>

<style lang="scss" scoped>
	.login_from {
		@apply border-solid border-#e5e5e5 uno-flex-y-center flex-justify-between flex-row p-y-2vh p-x-2vw
	}
</style>
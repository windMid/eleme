<template>
	<div class="header-wrapper">
		<div class="content">
			<div class="content-left">
				<img :src="seller.avatar" alt="avatar">
			</div>
			<div class="content-right">
				<div class="top">
					<span class="icon">
						
					</span>
					<span class="title">
						
					</span>
				</div>
				<div class="mid">
					
				</div>
				<div class="bottom">
					<span class="icon">
						
					</span>
					<span class="content">
						
					</span>
				</div>
			</div>
		</div>
		<div class="footer">
			<span class="icon">
				
			</span>
			<span class="content">
				
			</span>
			<span class="right-icon">
				
			</span>
		</div>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				seller: {},
			}
		},

		created() {
			this.$http.get('/seller').then((response) => {
				response = response.body
				if(response.errno === 0) {
					this.seller = response.data;
				}
			})
		}
	}
	
</script>

<style lang="stylus" rel="stylesheet/stylus">
	.header-wrapper
		background-color: #000
		.content
			background-color: #666
			.content-left
				margin:24px 16px 18px 24px
				display: inline-block
				img
					height: 64px
					width: 64px
</style>
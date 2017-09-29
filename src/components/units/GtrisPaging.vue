<template lang="html">
	<div class="gt-center">
		<div class="gt-pagination">
			<a href="javascript:void(0)" class="gt-pagination-nav"><i class="fa fa-angle-left"></i></a>
			<a href="javascript:void(0)" class="gt-pagination-nav"><i class="fa fa-angle-left"></i><i class="fa fa-angle-left"></i></a>
			<a href="javascript:void(0)" class="gt-pagination-num">1</a>
			<a href="javascript:void(0)" class="gt-pagination-num">2</a>
			<a href="javascript:void(0)" class="gt-pagination-num gt-active">3</a>
			<a href="javascript:void(0)" class="gt-pagination-num">4</a>
			<a href="javascript:void(0)" class="gt-pagination-num">5</a>
			<a href="javascript:void(0)" class="gt-pagination-num">6</a>
			<a href="javascript:void(0)" class="gt-pagination-nav"><i class="fa fa-angle-right"></i></a>
			<a href="javascript:void(0)" class="gt-pagination-nav"><i class="fa fa-angle-right"></i><i class="fa fa-angle-right"></i></a>
		</div>
	</div>
</template>

<script>
export default {
	name: 'gt-paging',
	data() {
		return 0
	},

	// TODO:
	// 1. 현 페이지가 첫 페이지면 맨 앞으로 이동과 이전 페이지 이동은 비활성화.
	// 2. 페이지를 몇 개 단위로 끊을지 결정
	// 3. 현 페이지가 마지막 페이지면 맨 끝으로 이동과 다음 페이지 이동은 비활성화
	//
	//
}
</script>

<style lang="scss">

</style>

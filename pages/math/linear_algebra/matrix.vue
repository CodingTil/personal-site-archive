<i18n lang="yaml">
en:
  title: "Linear Algebra"
  determinant: "Determinant"
  rank: "Rank"

de:
  title: "Lineare Algebra"
  determinant: "Determinant"
  rank: "Rang"
</i18n>

<template>
	<div>
		<h1>{{ $t("title") }}</h1>

		<!-- Matrix -->
		<div class="my-6">
			<div class="flex flew-row flex-wrap space-x-6 justify-between">
				<matrix-input v-model="array" />
				<div class="flex-grow">
					<section class="mb-6">
						<h2>{{ $t("determinant") }}</h2>
						<input
							disabled
							value="det A = a * b - c * d = 19"
							placerholder="det"
						/>
					</section>
					<hr />
					<section class="mt-6">
						<h2>{{ $t("rank") }}</h2>
						<span>Determinant</span>
						<input
							disabled
							value="det A = a * b - c * d = 19"
							placerholder="det"
						/>
					</section>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
export default {
	layout: "math-layout",
	head() {
		const i18nHead = this.$nuxtI18nHead({ addSeoAttributes: true });
		return {
			title: "Matrix | Til Mohr",
			htmlAttrs: {
				...i18nHead.htmlAttrs,
			},
			meta: [
				{
					hid: "description",
					name: "description",
					content: "Math - Linear Algebra - Matrix",
				},
				...i18nHead.meta,
			],
			link: [...i18nHead.link],
		};
	},
	data() {
		return {
			matrix: [],
		};
	},
};
</script>
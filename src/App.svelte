<script>
	import FeedbackList from './components/FeedbackList.svelte'
	let feedback = [
		{
			id: 1,
			rating: 5,
			title: 'Lorem Ipsum 1',
			text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.'
		},
		{
			id: 2,
			rating: 3,
			title: 'Lorem Ipsum 2',
			text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.'
		},
		{
			id: 3,
			rating: 1,
			title: 'Lorem Ipsum 3',
			text: 'Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry\'s standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.'
		},
	]
	$: count = feedback.length
	const deleteFeedback = (e) => {
		const itemId = e.detail;
		feedback = feedback.filter(item => item.id != itemId)
	}
</script>

<main class="container">
	{#if count === 0}
		Total Feedback is [0]
	{:else}
		Total Feedback is [{count}]
	{/if}
	<FeedbackList {feedback} on:delete-feedback={deleteFeedback} />
</main>


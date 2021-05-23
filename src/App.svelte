<script>
	const formValues ={
		name: '',
		profileSummary: '',
		country: '',
		jobLocation: [],
		remoteWork: false,
		skillSet: [],
		yearsOfExperience: ''
	}

	function submitForm(event) {
		console.log(formValues)
	}
</script>

<main>
	<div>
		<pre>
			{JSON.stringify(formValues, null, 2)}
		</pre>
	</div>
	<form on:submit|preventDefault={submitForm}>
		<div>
			<label for="name">Vorname</label>
			<!--Svelte casts the datatype accordingly to input type-->
			<input type="number" id="name" bind:value={formValues.name}>
		</div>

		<div>
			<label for="profile">Profile Summary</label>
			<textarea id="profile" bind:value={formValues.profileSummary} placeholder="Please enter some text"></textarea>
		</div>

		<div>
			<label for="country">Country</label>
			<select id="country" bind:value={formValues.country}>
				<option value="">Select a country</option>
				<option value="india">India</option>
				<option value="austria">Austria</option>
				<option value="england">England</option>
			</select>
		</div>

		<div>
			<label for="job-location">Job Location</label>
			<select 
				id="job-location" 
				bind:value={formValues.jobLocation}
				multiple
			>
				<option value="">Select a country</option>
				<option value="india">India</option>
				<option value="austria">Austria</option>
				<option value="england">England</option>
			</select>
		</div>

		<div>
			<input
				type="checkbox"
				id="remoteWork"
				bind:checked={formValues.remoteWork}
			/>
			<label for="remoteWork">Open for remote work?</label>
		</div>

		<div>
			<label>Skill set</label>
				<input
					type="checkbox"
					id="css"
					value="css"
					bind:group={formValues.skillSet}
				/>
				<label for="css">CSS</label>
				<input
					type="checkbox"
					id="html"
					value="html"
					bind:group={formValues.skillSet}
				/>
				<label for="css">HTML</label>
				<input
					type="checkbox"
					id="javascript"
					value="javascript"
					bind:group={formValues.skillSet}
				/>
				<label for="javascript">JavaScript</label>
		</div>

		<div>
			<label>Years of Experience</label>
				<input
					type="radio"
					id="1-2"
					value="1-2"
					bind:group={formValues.yearsOfExperience}
				/>
				<label for="1-2">1-2</label>
				<input
					type="radio"
					id="3-5"
					value="3-5"
					bind:group={formValues.yearsOfExperience}
				/>
				<label for="3-5">3-5</label>
				<input
					type="radio"
					id="5-10"
					value="5-10"
					bind:group={formValues.yearsOfExperience}
				/>
				<label for="5-10">5-10</label>
		</div>

		<div>
			<button>Submit</button>
		</div>
	</form>
</main>

<style>
	input + label {
		display: inline-flex;
	}

	main {
		/*text-align: center;*/
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
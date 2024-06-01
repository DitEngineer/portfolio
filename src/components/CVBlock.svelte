<script>
	export let productName = 'Stock';
	export let projectPart = 'Inventory Management System';
	export let timeSpan = '2024 -';

	let projects = [
		{
			projectName: 'eVenue',
			projectPart: 'Online Ticket Selling Platform',
			timeSpan: '2023 -'
		},
		{
			projectName: 'Stock',
			projectPart: 'Inventory Management System',
			timeSpan: '2024 -'
		},
		{
			projectName: 'OrderMatch',
			projectPart: 'WooCommerce and Shopify receipt checker',
			timeSpan: '2024 -'
		}
	];

	let educations = [
		{
			collegeName: 'FERI Maribor',
			collegeModule: 'Data Science',
			timeSpan: '2024 -'
		}
	];

	let skills = [
		'HTML',
		'CSS',
		'JavaScript',
		'React',
		'SvelteKit',
		'Database / API Integration',
		'Version Control System (Git)',
		'Debugging & Troubleshooting',
		'Web Development',
		'Web Testing'
	];

	let courses = [
		{
			name: 'The Complete JavaScript Course 2024: From Zero to Expert!',
			creator: 'Jonass Schmedtmann',
			date: '2023',
			link: 'https://www.udemy.com/course/the-complete-javascript-course/?couponCode=OF52424'
		},
		{
			name: 'The Advanced Web Developer Bootcamp',
			creator: ['Colt Steele', 'Elie Schoppik', 'Tim Garcia', 'Matt Lane'],
			date: '2024',
			link: 'https://www.udemy.com/course/the-advanced-web-developer-bootcamp/?couponCode=OF52424'
		}
	];
</script>

<div class="wrapper">
	<div class="box">
		<p class="cv-name">WORK EXPERIENCE</p>
		<ul>
			{#each projects as project}
				<li>
					<div class="info">
						<p class="name">{project.projectName}</p>
						<p class="description">{project.projectPart}</p>
					</div>
					<p class="time-span">{project.timeSpan}</p>
				</li>
			{/each}
		</ul>
	</div>

	<div class="box">
		<p class="cv-name">EDUCATION</p>
		<ul>
			{#each educations as education}
				<li>
					<div class="info">
						<p class="name">{education.collegeName}</p>
						<p class="description">{education.collegeModule}</p>
					</div>
					<p class="time-span">{education.timeSpan}</p>
				</li>
			{/each}
		</ul>
	</div>

	<div class="skill-box">
		<p class="cv-name">SKILLS & COMPETENCIES</p>
		<ul class="skill-list">
			{#each skills as skill}
				<li>{skill}</li>
			{/each}
		</ul>
	</div>

	<div class="box">
		<p class="cv-name">COURSES & CERTIFICATES</p>
		<ul>
			{#each courses as course}
				<li>
					<div class="info">
						<p class="name"><a href={course.link} class="course-link">{course.name}</a></p>
						<p class="description">{course.creator}</p>
					</div>
					<p class="time-span">{course.date}</p>
				</li>
			{/each}
		</ul>
	</div>
</div>

<style>
	* {
		padding: 0;
		margin: 0;
		box-sizing: border-box;

		z-index: 1;
	}

	.wrapper {
		height: 100%;
		width: max-content;

		overflow: auto;

		display: flex;
		flex-direction: column;
		gap: 56px;
	}

	.box {
		height: max-content;
		width: max-content;

		display: flex;
		flex-direction: column;
	}

	.cv-name {
		color: #a2a2a2;
		width: 320px;
		font-size: 14px;
		letter-spacing: 0.1rem;
		cursor: default;
	}

	ul {
		list-style-type: none;
		width: max-content;

		display: flex;
		flex-direction: column;
		gap: 56px;
	}

	ul li {
		height: max-content;
		width: 100%;

		display: flex;
		justify-content: space-between;
	}

	ul li:first-child {
		margin-top: 16px;
	}

	.info {
		height: max-content;
		width: 460px;

		font-size: 14px;
	}

	.info .name {
		color: #3b3d41;
		font-weight: 600;
		transition: 0.2s;
		cursor: pointer;
	}

	.info .name:hover {
		opacity: 0.7;
	}

	.info .description {
		color: #a2a2a2;
		cursor: default;
	}

	.time-span {
		height: 30px;
		width: max-content;

		white-space: nowrap;

		font-size: 14px;
		color: #a2a2a2;

		cursor: default;
	}

	.course-link {
		text-decoration: none;
		color: inherit;
	}

	@media screen and (max-width: 809.98px) {
		.wrapper {
			padding-bottom: 60px;
		}

		.box {
			margin-top: 40px;
			flex-direction: column;
			width: 100%;

			display: flex;
			justify-content: space-between;
		}

		.box ul li {
			width: calc(100vw - 76px);

			display: flex;
			justify-content: space-between;
		}

		.box ul li:first-child {
			margin-top: 16px;
		}

		.cv-name {
			width: max-content;
		}

		.info {
			width: max-content;
		}

		.skill-list {
			gap: 4px;
			font-size: 14px;
			list-style: circle;
		}

		.skill-list li:first-child {
			margin-top: 16px;
		}

		.skill-list li {
			font-weight: 500;
			color: #3b3d41;
		}
	}

	.skill-list {
		gap: 4px;
		font-size: 14px;
		font-weight: 500;
		color: #3b3d41;
	}

	.skill-list li:first-child {
		margin-top: 16px;
	}
</style>

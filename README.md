<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>DevOps Title Generator</title>
</head>
<body>
	<h2>Your DevOps title is:</h2>
	<p id='devOpsTitle'></p>
	<button type="button" onclick = changeTitle()>Get new title</button>
	<script type="text/javascript">
	function getName(){
		var start = [
			'Cloud',
			'Ops',
			'Dev',
			'Platform',
			'Build',
			'Reliability',
			'Release',
			'Site',
			'Automation',
			'Systems',
			'Kube'
		];

		var end = [
			'Engineer',
			'Architect'
		];

		const sample = start
			.map(x => ({ x, r: Math.random() }))
			.sort((a, b) => a.r - b.r)
			.map(a => a.x)
			.slice(0, 2);

		const suffix = end
			.map(x => ({ x, r: Math.random() }))
			.sort((a, b) => a.r - b.r)
			.map(a => a.x)
			.slice(0, 1);

		return sample[0] + sample[1] + ' ' + suffix[0];
	}
	function changeTitle(){
		document.getElementById('devOpsTitle').innerHTML = getName();
	}
	</script>
</body>
</html>

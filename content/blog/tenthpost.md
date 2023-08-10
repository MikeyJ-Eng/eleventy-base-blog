---
title: Responsive HTML Table
description: This is a post based on my TCG Bootcamp experience
date: 2023-08-07
tags:
  - Bootcamp Challenges
---
<head>
	<title>TCG: Semantic HTML Challenge Task</title>
	<meta name="viewport" content="width=device-width, initial-scale=1">
<!--	<link rel="stylesheet" href="tenthpost.css"> -->
	<link href='https://fonts.googleapis.com/css?family=Rock Salt' rel='stylesheet'>
    <style>
.h3 {
	font-family: "Helvetica Neu";
}

.h4 {
	font-family: "Rock Salt";
	font-size: 8px;
	text-align: right;
}

body {
	margin: 0;
	padding: 20px;
	font-family: "Helvetica Neu";
}

* {
	box-sizing: border-box;
}

.table {
	width: 100%;
	border-collapse: collapse;
	border: 2px solid purple;
}

.table th {
	padding: 10px 15px;
	border: 1px solid purple;
	color: #ffffff;
	background-image: url("https://cdn.glitch.me/8b1beacc-937c-4072-93d6-4ae825ab1a7a%2Fleopardskin.jpg"),
		linear-gradient(rgba(0, 0, 0, 0.1), rgba(0, 0, 0, 0.5));
	font-family: "Rock Salt";
	text-align: center;
	font-size: 8px;
	empty-cells: hide;
}

.table td {
	padding: 8px 15px;
	text-align: center;
	font-size: 12px;
}

.table tbody tr:nth-child(even) {
	background-color: #e495e4;
}

.table tbody tr:nth-child(odd) {
	background-color: #ff33cc;
}

/*responsive*/
@media(max-width: 500px) {
	.table thead {
		display: none;
	}

	.table,
	.table tbody,
	.table tr,
	.table td {
		display: block;
		width: 100%;
	}

	.table tr {
		margin-bottom: 15px;
	}

	.table td {
		text-align: right;
		padding-left: 50%;
		text-align: right;
		position: relative;
	}

	.table td::before {
		content: attr(data-label);
		position: absolute;
		left: 0;
		width: 50%;
		padding-left: 15px;
		font-size: 15px;
		font-weight: bold;
		text-align: left;
	}
}
    </style>
</head>
<body>
	<h3 class="h3">HTML/CSS Table Challenge</h3>
	<div style="overflow-x: auto;">
		<table class="table">
			<thead>
				<tr>
					<th>BAND</th>
					<th>YEAR FORMED</th>
					<th>NO. OF ALBUMS</th>
					<th>MOST FAMOUS SONG</th>
				</tr>
			</thead>

			<tbody>
				<!--"data-label" allows mobile device support-->
				<tr>
					<td data-label="BAND">Buzzcocks</td>
					<td data-label="YEAR FORMED">1976</td>
					<td data-label="NO. OF ALBUMS">9</td>
					<td data-label="MOST FAMOUS SONG">Ever fallen in love (with someone you shouldn't've)</td>
				</tr>

				<tr>
					<td data-label="BAND">The Clash</td>
					<td data-label="YEAR FORMED">1976</td>
					<td data-label="NO. OF ALBUMS">6</td>
					<td data-label="MOST FAMOUS SONG">London Calling</td>
				</tr>

				<tr>
					<td data-label="BAND">The Damned</td>
					<td data-label="YEAR FORMED">1976</td>
					<td data-label="NO. OF ALBUMS">10</td>
					<td data-label="MOST FAMOUS SONG">Smash it up</td>
				</tr>

				<tr>
					<td data-label="BAND">Sex Pistols</td>
					<td data-label="YEAR FORMED">1975</td>
					<td data-label="NO. OF ALBUMS">1</td>
					<td data-label="MOST FAMOUS SONG">Anarchy in the UK</td>
				</tr>

				<tr>
					<td data-label="BAND">Sham 69</td>
					<td data-label="YEAR FORMED">1976</td>
					<td data-label="NO. OF ALBUMS">13</td>
					<td data-label="MOST FAMOUS SONG">If The Kids Are United</td>
				</tr>

				<tr>
					<td data-label="BAND">Siouxsie and the Banshees</td>
					<td data-label="YEAR FORMED">1976</td>
					<td data-label="NO. OF ALBUMS">11</td>
					<td data-label="MOST FAMOUS SONG">Hong Kong Garden</td>
				</tr>

				<tr>
					<td data-label="BAND">Stiff Little Fingers</td>
					<td data-label="YEAR FORMED">1977</td>
					<td data-label="NO. OF ALBUMS">10</td>
					<td data-label="MOST FAMOUS SONG">Suspect Device</td>
				</tr>

				<tr>
					<td data-label="BAND">The Stranglers</td>
					<td data-label="YEAR FORMED">1974</td>
					<td data-label="NO. OF ALBUMS">17</td>
					<td data-label="MOST FAMOUS SONG">No More Heroes</td>
				</tr>
			</tbody>

			<tfoot>
				<tr>
					<th></th>
					<th>TOTAL ALBUMS</th>
					<th>77</th>
					<th></th>
				</tr>
			</tfoot>

		</table>
	</div>

	<h4 class="h4">A SUMMARY OF THE UK's MOST FAMOUS PUNK BANDS</h4>

</body>

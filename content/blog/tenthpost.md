---
title: Responsive HTML Table
description: This is a post based on my TCG Bootcamp experience
date: 2023-08-06
tags:
  - Bootcamp Challenges
---
<head>
	<title>TCG: Semantic HTML Challenge Task</title>
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" href="responsive_table_style.css">
	<link href='https://fonts.googleapis.com/css?family=Rock Salt' rel='stylesheet'>
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

<html><head>
		<title>HTML5 Canvas PONG game</title>
		
		<script type="text/javascript" src="lib/Game.js"></script>
		<script type="text/javascript" src="lib/Background.js"></script>
		<script type="text/javascript" src="lib/Paddle.js"></script>
		<script type="text/javascript" src="lib/Player.js"></script>
		<script type="text/javascript" src="lib/Opponent.js"></script>
		<script type="text/javascript" src="lib/Ball.js"></script>
		
		<style type="text/css">
		body
		{
			margin: 0px;
			padding: 0px;
			text-align: center;
		}
		
		canvas
		{
			margin: 0px auto;
		}
		
		fieldset
		{
			border: none;
		}
		
		label
		{
			display: block;
		}
		
		input
		{
			margin-bottom: 10px;
		}
		
		.controls
		{
			float: left;
			text-align: left;
		}
		
		.form
		{
			float: right;
			text-align: right;
		}
		
		.clear
		{
			clear: both;
		}
		
		.container
		{
			width: 740px;
			margin: 0px auto;
		}
		</style>
	</head>
	<body>
		<h1>HTML5 Canvas Game - Pong</h1>
		<div class="container">
			<canvas id="pong" width="740" height="640">
				This browser can not run this game (canvas support missing).
			</canvas>
			
			<div class="clear"></div>
			
			<div class="controls">
				<h3>Controls</h3>
				
				<h4>Player 1</h4>
				<ul>
					<li>Pause - P</li>
					<li>Left - Left Arrow</li>
					<li>Right - Right Arrow</li>
				</ul>
				
				<h4>Player 2</h4>
				<ul>
					<li>Pause - P</li>
					<li>Left - A</li>
					<li>Right - D</li>
				</ul>
			</div>
			
			<div class="form">
				<form action="#" method="get" id="settings">
					<fieldset>
						<label for="number_of_players">No. of Players</label>
						<input type="number" value="1" min="1" max="2" id="number_of_players" name="number_of_players">
					</fieldset>
					
					<fieldset>
						<label for="difficulty">Difficulty</label>
						<input type="number" value="5" min="1" id="difficulty" name="difficulty">
					</fieldset>
					
					<fieldset>
						<input type="button" name="start" value="Start" onclick="Javascript: startGame();">
					</fieldset>
				</form>
			</div>
			
			<div class="clear"></div>
		</div>
		
		<script type="text/javascript">
			var game = new Game("pong");
			function startGame()
			{
				var form = document.getElementById("settings");
				game.number_of_players = form.number_of_players.value;
				game.difficulty = form.difficulty.value;
				game.start();
			}
		</script>
	
</body></html>

# drag-and-drop-slider
<style>
	#div1 {
		width: 350px;
		height: 70px;
		padding: 10px;
		border: 1px solid #aaaaaa;
	}
</style>
<div id="div1" ondrop="drop(event)"
	ondragover="allowDrop(event)">
</div>
<br>

<img id="drag1" src=
<script>
	function allowDrop(ev) {
		ev.preventDefault();
	}

	function drag(ev) {
		ev.dataTransfer.setData("text", ev.target.id);
	}

	function drop(ev) {
		ev.preventDefault();
		var data = ev.dataTransfer.getData("text");
		ev.target.appendChild(document.getElementById(data));
	}
</script>

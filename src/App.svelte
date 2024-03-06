<script>
let files;
let previewAudio = false;

let audioUrl="";


let videoPreview=false;
function extractAudio(){
	var file = files[0];
	audioUrl = URL.createObjectURL(file);
	previewAudio = true;


}

</script>
<body>
	<input class="input" type="file" required accept="video/*" bind:files>
	<button on:click={extractAudio} class="button">Extract Audio</button>
	<div id="audioContainer"></div>
	{#if previewAudio}
	<audio width="60%" style="text-align: center;" id="uploadedaudio" controls src={audioUrl}>
	</audio>


		
	{/if}
</body>
<style>
	
body {
  font-family: Arial, sans-serif;
  text-align: center;
  margin: 20px;
}

.input {
  margin-bottom: 10px;
  
}

.button {
  padding: 10px;
  background-color:blue;
  color: white;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  
}

#audioContainer {
  margin-top: 20px;
 
}

audio {
  width: 60%;
  text-align: center;
  margin-top: 20px;
 
}

</style>
	
	  

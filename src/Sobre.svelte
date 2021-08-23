<script></script>

<svelte:head>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sobre</title>
</svelte:head>
    <div id="sobreBody">
    <h1>GAME OF FIFTEEN</h1>
    <h2>Group</h2>
    <ul>
      <li>Ênrell TSI; Tenho conhecimento em HTML5, básico em CSS3, JavaScript e Svelte</li><br>
      <li>Gabriel Miranda TSI; Reproduzo HTML5 básico, aprendendo CSS3 e JavaScript.</li>
      <li>Ezequias IPI; Tenho pouco conhecimento, em HTM5 E CSS3, mas está se esforçando para adquirir tais conhecimentos, para o auxilio do grupo.</li>
      <li><del>Alex David IPI</del></li>
      <li><del>Tiago IPI</del></li>
    </ul>
    <button class="button-2" id="buttonBack" onclick="window.location.href='./App.svelte'"><span>Back</span></button>
    </div>
    <style>
      @charset "UTF-8";
        :global(body) {
          margin: 0;
          padding: 0;
    
          background-color: #170126;
          color: #44D2F2;
        }
        .button-2 {
          display: inline-block;
          grid-area: button-2;
          text-align: center;

          padding: 0%;
          width: 100%;
          right: 100%;
          border: none;
          
          margin: 1%;
          cursor: pointer;
          transition: all 1s;
          transition-duration: 0.4s;
          outline: none;

          font: normal bolder 30px Arial, Helvetica, sans-serif;
          text-decoration: none;

          background-color: #270140;
          box-shadow: 0 10px #170126;
          color: #44D2F2;

        }
        .button-2 span {
          cursor: pointer;
          display: inline-block;
          position: relative;
          transition: 0.6s;
        }
        .button-2 span:after {
          content: "<<";
          position: absolute;
          opacity: 0;
          top: 0;
          right: -50px;
          transition: 0.6s;
        }
        .button-2:hover span {
          padding-right: 50px;
        }
        .button-2:hover span:after {
          opacity: 1;
          right: 0;
}
        .button-2:hover {
          background-color: #10001b;
        }
        .button-2:active {
          background-color: #10001b;
          box-shadow: 0 5px #10001b;
          transform: translateY(4px);
        }
        #sobreBody {
          color: white;
        }
        #buttonBack {
          width: 15%;
        }
    
    </style>

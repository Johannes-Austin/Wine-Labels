<!DOCTYPE html>
<html>
<head>
    <link href="https://fonts.googleapis.com/css2?family=Abril+Fatface&family=Alfa+Slab+One&family=Anton&family=Archivo+Black&family=Bangers&family=Bebas+Neue&family=Black+Ops+One&family=Boogaloo&family=Bowlby+One+SC&family=Bungee+Inline&family=Cabin+Sketch&family=Cherry+Cream+Soda&family=Chewy&family=Chilanka&family=Cinzel&family=Creepster&family=Dancing+Script&family=Ewert&family=Fascinate+Inline&family=Faster+One&family=Fredericka+the+Great&family=Frijole&family=Fugaz+One&family=Gloria+Hallelujah&family=Gravitas+One&family=Great+Vibes&family=Heebo&family=Iceberg&family=Indie+Flower&family=Jolly+Lodger&family=Julius+Sans+One&family=Kalam&family=Kaushan+Script&family=Luckiest+Guy&family=Metal+Mania&family=Monoton&family=Montserrat:wght@900&family=Mountains+of+Christmas&family=Mystery+Quest&family=Nosifer&family=Orbitron&family=Pacifico&family=Permanent+Marker&family=Press+Start+2P&family=Righteous&family=Rock+Salt&family=Rye&family=Shadows+Into+Light&family=Special+Elite&family=Staatliches&display=swap" rel="stylesheet">
    <style>
        body { margin: 0; padding: 0; }
        .controls { 
            background: #eee; padding: 15px; display: flex; gap: 10px; align-items: center; 
            border-bottom: 2px solid #ccc; flex-wrap: wrap; font-size: 14px;
        }
        .control-group { display: flex; align-items: center; gap: 5px; }
        .page-container { position: relative; width: 8.5in; height: 11in; margin: 0 auto; }
        .label-box { position: absolute; }
        .label-img { 
            width: 100%; height: 100%; 
            object-fit: contain; /* Prevents stretching */
            pointer-events: none; 
        }
        .text-container {
            position: absolute; width: 100%; text-align: center;
            top: 50%; left: 0; transform: translateY(-50%);
        }
        input[type="number"] { width: 50px; }
        
        @media print {
            .controls { display: none !important; }
            body { margin: 0; padding: 0; }
            .text-container div {
                -webkit-print-color-adjust: exact !important;
                print-color-adjust: exact !important;
                color-adjust: exact !important;
            }
        }
    </style>
</head>
<body>

<div class="controls">
    <select id="imageSelector">
        <option value="Juneberry.png">Juneberry</option>
        <option value="Cherry Wine.png">Cherry Wine</option>
		<option value="NewLabel.png">New Label Name</option>
    </select>
    
    <select id="fontSelector" style="width: 150px;"></select>

    <div class="control-group"><input type="checkbox" id="boldToggle"><b>Bold</b></div>
    <input type="text" id="line1" placeholder="Line 1">
    <input type="text" id="line2" placeholder="Line 2">
    
    <div class="control-group">Width:<input type="number" id="sizeInput" value="300">px</div>
    <div class="control-group">Height:<input type="number" id="heightInput" value="300">px</div>
    <div class="control-group">Spacing:<input type="number" id="spacingInput" value="10">px</div>
    <div class="control-group">Offset:<input type="number" id="offsetInput" value="0">px</div>
    <input type="color" id="fontColor" value="#000000">
    <input type="number" id="fontSize" value="20">px
    
    <button id="btnCopy">Copy Settings</button>
    <button id="btnPrint">Print</button>
</div>

<div class="page-container" id="container"></div>

<script>
    const fontList = ["Abril Fatface", "Alfa Slab One", "Anton", "Archivo Black", "Bangers", "Bebas Neue", "Black Ops One", "Boogaloo", "Bowlby One SC", "Bungee Inline", "Cabin Sketch", "Cherry Cream Soda", "Chewy", "Chilanka", "Cinzel", "Creepster", "Dancing Script", "Ewert", "Fascinate Inline", "Faster One", "Fredericka the Great", "Frijole", "Fugaz One", "Gloria Hallelujah", "Gravitas One", "Great Vibes", "Heebo", "Iceberg", "Indie Flower", "Jolly Lodger", "Julius Sans One", "Kalam", "Kaushan Script", "Luckiest Guy", "Metal Mania", "Monoton", "Montserrat", "Mountains of Christmas", "Mystery Quest", "Nosifer", "Orbitron", "Pacifico", "Permanent Marker", "Press Start 2P", "Righteous", "Rock Salt", "Rye", "Shadows Into Light", "Special Elite", "Staatliches"];

    const fontSelect = document.getElementById('fontSelector');
    fontList.forEach(font => {
        let opt = document.createElement('option');
        opt.value = `'${font}', cursive`;
        opt.innerHTML = font;
        opt.style.fontFamily = font;
        fontSelect.appendChild(opt);
    });

    const labelDefaults = {
        "Juneberry.png": {"l1":"Made: May 12th","l2":"1997","w":"354","h":"406","spacing":"-4","offset":"24","font":"'Boogaloo', cursive","fontSize":"22","color":"#000000","bold":false},
        "Cherry Wine.png": {"l1":"Made: May 12th","l2":"1997","w":"350","h":"350","spacing":"-2","offset":"-18","font":"'Boogaloo', cursive","fontSize":"24","color":"#ffafaf","bold":false}
    };

    function updateView() {
        const imgName = document.getElementById('imageSelector').value;
        const container = document.getElementById('container');
        container.innerHTML = '';
        for(let i=0; i<5; i++) {
            container.innerHTML += `
                <div class="label-box" id="box-${i}">
                    <img src="${imgName}" class="label-img">
                    <div class="text-container" id="text-container-${i}">
                        <div id="out1-${i}"></div>
                        <div id="out2-${i}"></div>
                    </div>
                </div>`;
        }
        updateLayout();
        updateText();
    }

    function updateLayout() {
        const w = document.getElementById('sizeInput').value + 'px';
        const h = document.getElementById('heightInput').value + 'px';
        const boxes = document.querySelectorAll('.label-box');
        const coords = [{top:'5%',left:'5%'}, {top:'5%',right:'5%'}, {top:'50%',left:'50%',trans:'translate(-50%,-50%)'}, {bottom:'5%',left:'5%'}, {bottom:'5%',right:'5%'}];
        boxes.forEach((box, i) => {
            box.style.width = w; box.style.height = h;
            Object.assign(box.style, coords[i]);
            if(coords[i].trans) box.style.transform = coords[i].trans;
        });
    }

    function updateText() {
        const cfg = {
            l1: document.getElementById('line1').value,
            l2: document.getElementById('line2').value,
            color: document.getElementById('fontColor').value,
            font: document.getElementById('fontSelector').value,
            size: document.getElementById('fontSize').value + 'px',
            spacing: document.getElementById('spacingInput').value + 'px',
            offset: document.getElementById('offsetInput').value + 'px',
            bold: document.getElementById('boldToggle').checked ? 'bold' : 'normal'
        };
        for(let i=0; i<5; i++) {
            const el1 = document.getElementById(`out1-${i}`);
            const el2 = document.getElementById(`out2-${i}`);
            const container = document.getElementById(`text-container-${i}`);
            el1.innerText = cfg.l1; el2.innerText = cfg.l2;
            [el1, el2].forEach(el => { el.style.fontSize = cfg.size; el.style.color = cfg.color; el.style.fontFamily = cfg.font; el.style.fontWeight = cfg.bold; });
            el1.style.marginBottom = cfg.spacing;
            container.style.marginTop = cfg.offset;
        }
    }

    function loadDefaults() {
        const type = document.getElementById('imageSelector').value;
        const cfg = labelDefaults[type] || labelDefaults["Juneberry.png"];
        document.getElementById('line1').value = cfg.l1;
        document.getElementById('line2').value = cfg.l2;
        document.getElementById('sizeInput').value = cfg.w;
        document.getElementById('heightInput').value = cfg.h;
        document.getElementById('spacingInput').value = cfg.spacing;
        document.getElementById('offsetInput').value = cfg.offset;
        document.getElementById('fontSelector').value = cfg.font;
        document.getElementById('fontSize').value = cfg.fontSize;
        document.getElementById('fontColor').value = cfg.color;
        document.getElementById('boldToggle').checked = cfg.bold;
        updateView();
    }

    document.getElementById('imageSelector').addEventListener('change', loadDefaults);
    document.getElementById('fontSelector').addEventListener('change', updateText);
    document.getElementById('boldToggle').addEventListener('change', updateText);
    document.getElementById('line1').addEventListener('input', updateText);
    document.getElementById('line2').addEventListener('input', updateText);
    document.getElementById('sizeInput').addEventListener('input', updateLayout);
    document.getElementById('heightInput').addEventListener('input', updateLayout);
    document.getElementById('spacingInput').addEventListener('input', updateText);
    document.getElementById('offsetInput').addEventListener('input', updateText);
    document.getElementById('fontColor').addEventListener('input', updateText);
    document.getElementById('fontSize').addEventListener('input', updateText);
    document.getElementById('btnPrint').addEventListener('click', () => window.print());
    document.getElementById('btnCopy').addEventListener('click', () => {
        const settings = {
            l1: document.getElementById('line1').value,
            l2: document.getElementById('line2').value,
            w: document.getElementById('sizeInput').value,
            h: document.getElementById('heightInput').value,
            spacing: document.getElementById('spacingInput').value,
            offset: document.getElementById('offsetInput').value,
            font: document.getElementById('fontSelector').value,
            fontSize: document.getElementById('fontSize').value,
            color: document.getElementById('fontColor').value,
            bold: document.getElementById('boldToggle').checked
        };
        navigator.clipboard.writeText(JSON.stringify(settings));
        alert("Settings copied!");
    });

    loadDefaults();
</script>
</body>
</html>

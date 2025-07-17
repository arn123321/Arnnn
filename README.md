<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ficha de Treinador Pokémon Fire Red</title>
    <link href="https://fonts.cdnfonts.com/css/pokemon-solid" rel="stylesheet">
    <link href="https://fonts.cdnfonts.com/css/press-start-2p" rel="stylesheet">
    <style>
        :root {
            --fire-red-border: #222;
            --fire-red-bg-light: #F0F0F0;
            --fire-red-bg-dark: #A0A0A0;
            --fire-red-text: #222;
            --fire-red-font-pixel: 'Press Start 2P', cursive;
            --fire-red-font-title: 'Pokemon Solid', sans-serif;
        }

        body {
            font-family: var(--fire-red-font-pixel);
            background-color: #333;
            color: var(--fire-red-text);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
            padding: 10px;
            box-sizing: border-box;
            overflow-y: auto;
            background-image: linear-gradient(to bottom, #3a6186, #89253e);
        }

        .game-container {
            width: 100%;
            max-width: 800px;
            background-color: var(--fire-red-bg-light);
            border: 4px solid var(--fire-red-border);
            border-radius: 8px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.7);
            display: flex;
            flex-direction: column;
            overflow: hidden;
            box-sizing: border-box;
        }

        .header {
            background-color: #e74c3c;
            border-bottom: 2px solid var(--fire-red-border);
            padding: 10px 15px;
            text-align: center;
            font-size: 1.3em;
            color: #fff;
            text-shadow: 1px 1px var(--fire-red-border);
            font-family: var(--fire-red-font-title);
            letter-spacing: 1px;
        }

        .tabs-nav {
            display: flex;
            background-color: var(--fire-red-bg-dark);
            border-bottom: 2px solid var(--fire-red-border);
            overflow-x: auto;
            white-space: nowrap;
        }

        .tabs-nav button {
            flex: 1;
            padding: 10px 8px;
            border: none;
            background-color: var(--fire-red-bg-dark);
            color: #fff;
            font-family: var(--fire-red-font-pixel);
            font-size: 0.6em;
            cursor: pointer;
            border-right: 1px solid var(--fire-red-border);
            transition: background-color 0.2s, color 0.2s;
            text-shadow: 1px 1px var(--fire-red-border);
        }

        .tabs-nav button:last-child {
            border-right: none;
        }

        .tabs-nav button:hover {
            background-color: #888;
        }

        .tabs-nav button.active {
            background-color: var(--fire-red-bg-light);
            color: var(--fire-red-text);
            border-top: 2px solid var(--fire-red-border);
            border-left: 2px solid var(--fire-red-border);
            border-right: 2px solid var(--fire-red-border);
            border-bottom: none;
            margin-top: -2px;
            padding-top: 12px;
            box-shadow: inset 0 2px 2px rgba(0, 0, 0, 0.1);
            text-shadow: none;
            position: relative;
            z-index: 1;
        }

        .tab-content {
            padding: 15px;
            background-color: var(--fire-red-bg-light);
            flex-grow: 1;
            overflow-y: auto;
            max-height: calc(98vh - 140px);
            display: none;
            box-sizing: border-box;
        }

        .tab-content.active {
            display: block;
        }

        .form-group {
            margin-bottom: 10px;
            display: flex;
            flex-direction: column;
        }

        .form-group label {
            font-family: var(--fire-red-font-pixel);
            font-size: 0.7em;
            margin-bottom: 3px;
            color: var(--fire-red-text);
        }

        .form-group input,
        .form-group input::placeholder,
        .form-group select {
            background-color: #E0E0E0;
            border: 2px solid var(--fire-red-border);
            padding: 6px;
            font-family: var(--fire-red-font-pixel);
            font-size: 0.75em;
            color: var(--fire-red-text);
            box-sizing: border-box;
            border-radius: 3px;
        }

        .form-group input:focus,
        .form-group select:focus {
            outline: none;
            border-color: #555;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
        }

        .form-group input::placeholder {
            color: #777;
        }

        .button-group button,
        .action-button {
            background-color: #60a0f0;
            color: white;
            border: 2px solid var(--fire-red-border);
            padding: 6px 10px;
            font-family: var(--fire-red-font-pixel);
            font-size: 0.7em;
            cursor: pointer;
            border-radius: 3px;
            text-shadow: 1px 1px var(--fire-red-border);
            transition: background-color 0.2s, box-shadow 0.2s;
            box-shadow: 2px 2px var(--fire-red-border);
        }

        .button-group button:hover,
        .action-button:hover {
            background-color: #5090e0;
            box-shadow: 1px 1px var(--fire-red-border);
        }

        .action-button.red {
            background-color: #e04040;
        }
        .action-button.red:hover {
            background-color: #c03030;
        }

        .character-avatar {
            width: 120px;
            height: 120px;
            border: 2px solid var(--fire-red-border);
            background-color: #D0D0D0;
            display: block;
            margin: 0 auto 10px;
            background-size: cover;
            background-position: center;
            image-rendering: pixelated;
        }

        .money-control {
            display: flex;
            align-items: center;
            gap: 5px;
            margin-bottom: 10px;
            flex-wrap: nowrap;
            justify-content: flex-start;
        }

        .money-control .money-button {
            background-color: #70b070;
            color: white;
            border: 2px solid #3a603a;
            border-radius: 5px;
            padding: 5px 8px;
            font-family: var(--fire-red-font-pixel);
            font-size: 0.7em;
            cursor: pointer;
            text-shadow: 1px 1px #3a603a;
            box-shadow: 2px 2px #3a603a;
            transition: background-color 0.1s, box-shadow 0.1s;
        }

        .money-control .money-button:hover {
            background-color: #60a060;
            box-shadow: 1px 1px #3a603a;
        }
        .money-control .money-button.negative {
            background-color: #e07070;
            border-color: #803030;
            text-shadow: 1px 1px #803030;
            box-shadow: 2px 2px #803030;
        }
        .money-control .money-button.negative:hover {
            background-color: #c06060;
            box-shadow: 1px 1px #803030;
        }
        .money-control .money-button.single-unit {
            width: 30px;
            height: 30px;
            min-width: unset;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 1.2em;
        }

        .money-control input {
            flex-grow: 0;
            width: 80px;
            text-align: center;
        }

        .item-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(90px, 1fr));
            gap: 10px;
            margin-top: 5px;
        }

        .item-card {
            border: 2px solid var(--fire-red-border);
            background-color: #E8E8E8;
            padding: 8px;
            text-align: center;
            border-radius: 5px;
            display: flex;
            flex-direction: column;
            align-items: center;
            position: relative;
            transition: background-color 0.2s;
        }

        .item-card:hover {
            background-color: #D0D0D0;
        }

        .item-card img {
            width: 48px;
            height: 48px;
            object-fit: contain;
            image-rendering: pixelated;
            margin-bottom: 3px;
        }

        .item-card p {
            font-family: var(--fire-red-font-pixel);
            font-size: 0.65em;
            margin: 3px 0;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
            width: 100%;
        }

        .item-card .quantity-control {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 3px;
            margin-top: 5px;
            width: 100%;
            padding: 0 5px;
        }

        .item-card .quantity-control input {
            flex-grow: 0;
            width: 40px;
            text-align: center;
            padding: 2px;
            font-size: 0.6em;
            height: 22px;
            box-sizing: border-box;
        }

        .item-card .quantity-control button {
            width: 22px;
            height: 22px;
            min-width: 22px;
            font-size: 0.8em;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            border-width: 1px;
        }

        .pokemon-card img {
            width: 120px;
            height: 120px;
            object-fit: contain;
            image-rendering: pixelated;
            margin-bottom: 8px;
        }

        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 10px;
            margin-top: 5px;
        }

        .pokemon-card {
            border: 2px solid var(--fire-red-border);
            background-color: #E8E8E8;
            padding: 10px;
            border-radius: 5px;
            display: flex;
            flex-direction: column;
            align-items: center;
            position: relative;
            box-sizing: border-box;
        }

        .pokemon-card .info-container {
            display: flex;
            flex-direction: column;
            flex-grow: 1;
            width: 100%;
            align-items: center;
        }

        .pokemon-card select {
            width: calc(100% - 10px);
            margin-bottom: 5px;
            font-size: 0.75em;
            padding: 4px;
            box-sizing: border-box;
        }

        .pokemon-card .form-group {
            width: calc(100% - 10px);
            margin-bottom: 5px;
            align-items: center;
        }
        .pokemon-card .form-group label {
            width: 100%;
            text-align: center;
        }

        .pokemon-card .stat-control {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 8px;
            width: 100%;
        }

        .pokemon-card .stat-control input {
            flex-grow: 1;
            max-width: 60px;
            text-align: center;
            font-size: 0.75em;
            padding: 3px;
            height: 25px;
            box-sizing: border-box;
            background-color: #D0E0F0;
        }
         .pokemon-card .stat-control input.hp {
            background-color: #E0FFD0;
        }

        .pokemon-card .stat-control button {
            width: 28px;
            height: 28px;
            min-width: unset;
            font-size: 1.1em;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            box-shadow: 1px 1px var(--fire-red-border);
        }
        .pokemon-card .stat-control button:hover {
            box-shadow: 0 0 var(--fire-red-border);
        }

        .pokemon-card .action-button.red {
            margin-top: 10px;
            font-size: 0.65em;
            padding: 5px;
            width: calc(100% - 10px);
        }

        .pokedex-container {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }
        
        .pokedex-top-panel {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }
        
        .pokedex-details {
            flex: 1;
            min-width: 300px;
            border: 2px solid var(--fire-red-border);
            border-radius: 5px;
            padding: 10px;
            background-color: #E8E8E8;
            min-height: 300px;
            display: none;
            position: sticky;
            top: 0;
            z-index: 100;
            background-color: #E8E8E8;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
            max-height: calc(100vh - 200px);
            overflow-y: auto;
        }
        
        .pokedex-details.fixed {
            position: fixed;
            top: 20px;
            right: 20px;
            width: 300px;
            max-height: 80vh;
            z-index: 1000;
            box-shadow: 0 0 20px rgba(0,0,0,0.5);
        }
        
        .pokedex-details.active {
            display: block;
        }
        
        .pokedex-grid-container {
            flex: 2;
            min-height: 400px;
        }
        
        .pokedex-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(70px, 1fr));
            gap: 5px;
            margin-top: 5px;
        }
        
        .pokedex-entry {
            border: 1px solid var(--fire-red-border);
            background-color: #E8E8E8;
            padding: 3px;
            text-align: center;
            border-radius: 3px;
            display: flex;
            flex-direction: column;
            align-items: center;
            cursor: pointer;
            position: relative;
        }
        
        .pokedex-entry.selected {
            border: 2px solid #e74c3c;
            background-color: #d0d0d0;
        }
        
        .pokedex-entry img {
            width: 64px;
            height: 64px;
            object-fit: contain;
            image-rendering: pixelated;
            filter: grayscale(100%) brightness(0%);
            transition: filter 0.2s;
        }
        
        .pokedex-entry.seen img {
            filter: grayscale(0%) brightness(100%);
        }
        
        .pokedex-entry .pokemon-name-hover {
            position: absolute;
            bottom: -18px;
            left: 50%;
            transform: translateX(-50%);
            background-color: rgba(0, 0, 0, 0.8);
            color: white;
            padding: 2px 5px;
            border-radius: 3px;
            font-family: var(--fire-red-font-pixel);
            font-size: 0.5em;
            white-space: nowrap;
            z-index: 10;
            opacity: 0;
            visibility: hidden;
            transition: opacity 0.2s, visibility 0.2s;
        }
        
        .pokedex-entry:hover .pokemon-name-hover {
            opacity: 1;
            visibility: visible;
        }
        
        .pokemon-details-header {
            display: flex;
            align-items: center;
            margin-bottom: 10px;
        }
        
        .pokemon-details-image {
            width: 100px;
            height: 100px;
            border: 2px solid var(--fire-red-border);
            background-color: #D0D0D0;
            margin-right: 15px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .pokemon-details-image img {
            width: 90%;
            height: 90%;
            object-fit: contain;
            image-rendering: pixelated;
        }
        
        .pokemon-details-info {
            flex: 1;
        }
        
        .pokemon-details-name {
            font-size: 0.9em;
            margin-bottom: 5px;
            text-align: left;
        }
        
        .pokemon-details-types {
            display: flex;
            gap: 5px;
            margin-top: 5px;
        }
        
        .pokemon-type {
            padding: 3px 8px;
            border-radius: 10px;
            color: white;
            font-size: 0.6em;
            text-shadow: 1px 1px var(--fire-red-border);
        }
        
        .pokemon-stats {
            margin-top: 15px;
        }
        
        .stat-row {
            display: flex;
            margin-bottom: 5px;
            align-items: center;
        }
        
        .stat-name {
            width: 100px;
            font-size: 0.6em;
            text-align: left;
        }
        
        .stat-bar-container {
            flex: 1;
            height: 12px;
            background-color: #ccc;
            border-radius: 5px;
            overflow: hidden;
            position: relative;
        }
        
        .stat-bar {
            height: 100%;
            background-color: #4caf50;
            transition: width 0.3s ease;
        }
        
        .stat-value {
            width: 40px;
            text-align: right;
            font-size: 0.6em;
            margin-left: 5px;
        }
        
        .seen-toggle {
            margin-top: 15px;
            text-align: center;
        }
        
        .pin-button-container {
            position: absolute;
            top: 10px;
            right: 10px;
        }
        
        .pin-button {
            background: #f0c000;
            border: 2px solid #8a6d00;
            border-radius: 50%;
            width: 30px;
            height: 30px;
            cursor: pointer;
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 16px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.3);
        }
        
        .pin-button.fixed {
            background: #f0f000;
        }
        
        .pin-button:hover {
            background: #ffd700;
        }

        .trainer-summary {
            margin-top: 15px;
            border-top: 2px solid var(--fire-red-border);
            padding-top: 15px;
        }

        .summary-section {
            margin-bottom: 15px;
        }

        .summary-section h3 {
            margin-top: 0;
            margin-bottom: 8px;
            font-size: 0.8em;
            text-align: center;
        }

        .team-preview {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 10px;
            margin-bottom: 10px;
        }

        .team-slot {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 8px;
            background-color: #E8E8E8;
            border: 2px solid var(--fire-red-border);
            border-radius: 5px;
        }

        .team-slot img {
            width: 80px;
            height: 80px;
            object-fit: contain;
            image-rendering: pixelated;
            margin-bottom: 5px;
        }

        .hp-bar-container {
            width: 100%;
            height: 10px;
            background-color: #ccc;
            border-radius: 5px;
            overflow: hidden;
            position: relative;
        }

        .hp-bar {
            height: 100%;
            transition: width 0.3s ease;
        }

        .hp-info {
            font-size: 0.6em;
            margin-top: 3px;
            text-align: center;
            font-family: var(--fire-red-font-pixel);
        }
        
        .level-info {
            font-size: 0.6em;
            margin-top: 2px;
            text-align: center;
            font-family: var(--fire-red-font-pixel);
        }

        .pokedex-summary {
            text-align: center;
            font-size: 0.8em;
            margin-bottom: 10px;
            font-family: var(--fire-red-font-pixel);
        }

        .items-preview {
            display: flex;
            flex-wrap: wrap;
            gap: 5px;
            justify-content: center;
        }

        .item-preview {
            width: 32px;
            height: 32px;
            border: 1px solid var(--fire-red-border);
            background-color: #D0D0D0;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        .item-preview img {
            max-width: 100%;
            max-height: 100%;
            image-rendering: pixelated;
        }

        .item-quantity {
            position: absolute;
            bottom: 0;
            right: 0;
            background-color: rgba(0,0,0,0.7);
            color: white;
            font-size: 0.5em;
            padding: 1px 3px;
            border-radius: 3px 0 0 0;
        }

        .attacks-container {
            overflow-y: auto;
            max-height: 500px;
            border: 2px solid var(--fire-red-border);
            border-radius: 5px;
            padding: 10px;
            margin-top: 10px;
            background-color: #E8E8E8;
        }
        
        .attack-type-section {
            margin-bottom: 20px;
            border-bottom: 2px solid var(--fire-red-border);
            padding-bottom: 10px;
        }
        
        .attack-type-section h3 {
            background-color: var(--fire-red-bg-dark);
            color: white;
            padding: 5px;
            text-align: center;
            border-radius: 4px;
            font-size: 0.8em;
            margin-top: 0;
        }
        
        .attack-table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.65em;
        }
        
        .attack-table th {
            background-color: var(--fire-red-bg-dark);
            color: white;
            padding: 5px;
            text-align: left;
            position: sticky;
            top: 0;
        }
        
        .attack-table td {
            padding: 5px;
            border-bottom: 1px solid var(--fire-red-border);
        }
        
        .attack-table tr:nth-child(even) {
            background-color: #F0F0F0;
        }
        
        .attack-table tr:hover {
            background-color: #D0D0D0;
        }
        
        .attack-name {
            font-weight: bold;
        }
        
        .attack-activation {
            text-align: center;
            white-space: nowrap;
        }
        
        .pokedex-search-container {
            margin-bottom: 15px;
            padding: 0 5px;
        }

        #pokedex-search-input {
            font-size: 0.8em;
            padding: 8px;
            border: 2px solid var(--fire-red-border);
            border-radius: 4px;
            background-color: #E0E0E0;
            width: 100%;
            box-sizing: border-box;
        }

        /* Novos estilos para a seção de movimentos */
        .pokemon-moves {
            margin-top: 15px;
            border-top: 2px solid var(--fire-red-border);
            padding-top: 15px;
        }
        
        .moves-table {
            width: 100%;
            border-collapse: collapse;
            font-size: 0.6em;
            margin-top: 10px;
        }
        
        .moves-table th {
            background-color: var(--fire-red-border);
            color: white;
            padding: 5px;
            text-align: left;
        }
        
        .moves-table td {
            padding: 5px;
            border-bottom: 1px solid var(--fire-red-border);
        }
        
        .moves-table tr:nth-child(even) {
            background-color: #F0F0F0;
        }
        
        .move-name {
            font-weight: bold;
        }
        
        .move-type {
            padding: 2px 5px;
            border-radius: 3px;
            color: white;
            text-shadow: 1px 1px var(--fire-red-border);
        }
        
        .move-method {
            text-align: center;
        }
        
        .move-power {
            text-align: center;
        }
        
        .move-accuracy {
            text-align: center;
        }
        
        .move-pp {
            text-align: center;
        }
        
        .moves-loading {
            text-align: center;
            font-size: 0.8em;
            padding: 10px;
        }

        @media (max-width: 480px) {
            .tabs-nav button {
                font-size: 0.5em;
                padding: 8px 3px;
                min-width: 60px;
            }

            .team-grid {
                grid-template-columns: 1fr;
            }

            .pokemon-card {
                flex-direction: column;
                align-items: center;
                text-align: center;
            }

            .pokemon-card img {
                margin-right: 0;
                margin-bottom: 5px;
            }
             .pokemon-card .info-container {
                width: 100%;
                align-items: center;
            }
            .pokemon-card .form-group {
                width: 90%;
            }
            .pokemon-card select {
                width: 90%;
            }
            
            .team-preview {
                grid-template-columns: repeat(3, 1fr);
            }
            
            .attack-table {
                font-size: 0.5em;
            }
            
            .pokedex-details.fixed {
                position: fixed;
                top: 10px;
                right: 10px;
                left: 10px;
                width: auto;
                max-height: 50vh;
            }
            
            #pokedex-search-input {
                font-size: 0.7em;
                padding: 6px;
            }
            
            .moves-table {
                font-size: 0.5em;
            }
            
            .moves-table th, .moves-table td {
                padding: 3px;
            }
        }
        
        @media (max-width: 768px) {
            .pokedex-top-panel {
                flex-direction: column;
            }
            
            .pokedex-details {
                position: relative;
                top: auto;
                z-index: auto;
                box-shadow: none;
                max-height: none;
            }
            
            .pokedex-grid-container {
                width: 100%;
            }
        }
    </style>
</head>
<body>

    <div class="game-container">
        <div class="header">
            Ficha de Treinador Pokémon
        </div>

        <div class="tabs-nav">
            <button class="tab-button active" data-tab="character">Personagem</button>
            <button class="tab-button" data-tab="backpack">Mochila</button>
            <button class="tab-button" data-tab="team">Equipe</button>
            <button class="tab-button" data-tab="pokedex">Pokédex</button>
            <button class="tab-button" data-tab="attacks">Ataques</button>
        </div>
        <div id="character" class="tab-content active">
            <h2>Personagem</h2>

            <div class="character-avatar" id="character-avatar" style="background-image: url('https://www.serebii.net/fireleaf/red.gif');"></div>
            
            <div class="form-group">
                <label for="avatar-file">Selecionar Avatar:</label>
                <input type="file" id="avatar-file" accept="image/*" style="font-size: 0.65em; width: 100%;">
            </div>

            <div class="form-group">
                <label for="character-name">Nome do Personagem:</label>
                <input type="text" id="character-name" value="RED" maxlength="12" onchange="saveData()">
            </div>

            <div class="form-group">
                <label for="money">Dinheiro:</label>
                <div class="money-control">
                    <button class="money-button negative single-unit" onclick="adjustMoney(-1)">-</button>
                    <input type="number" id="money" value="3500" min="0" onchange="saveData()">
                    <button class="money-button single-unit" onclick="adjustMoney(1)">+</button>
                </div>
            </div>

            <div class="trainer-summary">
                <div class="summary-section">
                    <h3>Resumo do Treinador</h3>
                    
                    <div class="team-preview" id="team-preview">
                    </div>
                    
                    <div class="pokedex-summary" id="pokedex-summary">
                        Pokédex: 0/493
                    </div>
                    
                    <div class="items-preview" id="items-preview">
                    </div>
                </div>
            </div>
        </div>

        <div id="backpack" class="tab-content">
            <h2>Mochila</h2>
            <div class="item-list" id="item-list">
            </div>
        </div>

        <div id="team" class="tab-content">
            <h2>Equipe Pokémon</h2>
            <div class="team-grid" id="team-grid">
            </div>
            
            <div class="form-group">
                <label for="pokemon-search">Buscar Pokémon:</label>
                <input type="text" id="pokemon-search" placeholder="Digite o nome do Pokémon..." oninput="filterPokemonList()" style="width: 100%;">
            </div>

            <button class="action-button" onclick="addPokemonSlot()">Adicionar Pokémon</button>
        </div>

        <div id="pokedex" class="tab-content">
            <h2>Pokédex</h2>
            <div class="pokedex-container">
                <div class="pokedex-top-panel">
                    <div class="pokedex-details" id="pokedex-details">
                        <div class="loading-message">Selecione um Pokémon para ver os detalhes</div>
                    </div>
                    
                    <div class="pokedex-grid-container">
                        <div class="pokedex-search-container">
                            <input type="text" id="pokedex-search-input" placeholder="Buscar Pokémon por nome ou número..." 
                                   oninput="filterPokedex(this.value)">
                        </div>
                        
                        <div class="pokedex-grid" id="pokedex-grid">
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div id="attacks" class="tab-content">
            <h2>Ataques</h2>
            <div class="attacks-container" id="attacks-container">
            </div>
        </div>
    </div>

    <script>
        // Variáveis globais
        let characterData = {
            avatarUrl: 'https://www.serebii.net/fireleaf/red.gif',
            name: 'RED',
            money: 3500,
        };

        const backpackItems = [
            { name: "Potion", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/potion.png", quantity: 0 },
            { name: "Super Potion", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/super-potion.png", quantity: 0 },
            { name: "Hyper Potion", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/hyper-potion.png", quantity: 0 },
            { name: "Full Restore", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/full-restore.png", quantity: 0 },
            { name: "Poké Ball", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/poke-ball.png", quantity: 0 },
            { name: "Great Ball", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/great-ball.png", quantity: 0 },
            { name: "Ultra Ball", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/ultra-ball.png", quantity: 0 },
            { name: "Master Ball", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/master-ball.png", quantity: 0 },
            { name: "Antidote", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/antidote.png", quantity: 0 },
            { name: "Paralyze Heal", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/paralyze-heal.png", quantity: 0 },
            { name: "Burn Heal", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/burn-heal.png", quantity: 0 },
            { name: "Ice Heal", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/ice-heal.png", quantity: 0 },
            { name: "Awakening", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/awakening.png", quantity: 0 },
            { name: "Full Heal", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/full-heal.png", quantity: 0 },
            { name: "Repel", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/repel.png", quantity: 0 },
            { name: "Super Repel", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/super-repel.png", quantity: 0 },
            { name: "Max Repel", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/max-repel.png", quantity: 0 },
            { name: "Rare Candy", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/rare-candy.png", quantity: 0 },
            { name: "Fire Stone", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/fire-stone.png", quantity: 0 },
            { name: "Water Stone", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/water-stone.png", quantity: 0 },
            { name: "Thunder Stone", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/thunder-stone.png", quantity: 0 },
            { name: "Leaf Stone", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/leaf-stone.png", quantity: 0 },
            { name: "Moon Stone", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/moon-stone.png", quantity: 0 },
            { name: "Sun Stone", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/sun-stone.png", quantity: 0 },
            { name: "Leftovers", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/leftovers.png", quantity: 0 },
            { name: "Choice Band", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/choice-band.png", quantity: 0 },
            { name: "Focus Sash", sprite: "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/items/focus-sash.png", quantity: 0 },
        ];

        let teamPokemon = [];
        let pokedexSeen = [];
        let isPokedexFixed = false;
        let pokemonSlotCount = 0;

        const pokemonList = [];
        for (let i = 1; i <= 493; i++) {
            pokemonList.push({
                id: i,
                name: "Pokémon #" + String(i).padStart(3, '0'),
                sprite: `https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/${i}.png`
            });
        }

        const attackData = [
            // ... (lista de ataques permanece a mesma)
        ];

        // Função para salvar dados no localStorage
        function saveData() {
            characterData.avatarUrl = document.getElementById('character-avatar').style.backgroundImage.replace(/url\(['"]?(.*?)['"]?\)/, '$1');
            characterData.name = document.getElementById('character-name').value;
            characterData.money = parseInt(document.getElementById('money').value);

            localStorage.setItem('characterData', JSON.stringify(characterData));

            const currentBackpackItems = [];
            document.querySelectorAll('#item-list .item-card').forEach(itemCard => {
                const name = itemCard.querySelector('p').textContent;
                const quantity = parseInt(itemCard.querySelector('input').value);
                const originalItem = backpackItems.find(item => item.name === name);
                if (originalItem) {
                    currentBackpackItems.push({ name: name, sprite: originalItem.sprite, quantity: quantity });
                }
            });
            localStorage.setItem('backpackItems', JSON.stringify(currentBackpackItems));

            const currentTeam = [];
            document.querySelectorAll('#team-grid .pokemon-card').forEach(pokemonCard => {
                const pokemonId = pokemonCard.querySelector('select').value;
                const hpCurrent = parseInt(pokemonCard.querySelector(`#hp-current-${pokemonCard.dataset.slotId}`).value);
                const hpMax = parseInt(pokemonCard.querySelector(`#hp-max-${pokemonCard.dataset.slotId}`).value);
                const atk = parseInt(pokemonCard.querySelector(`#atk-current-${pokemonCard.dataset.slotId}`).value);
                const def = parseInt(pokemonCard.querySelector(`#def-current-${pokemonCard.dataset.slotId}`).value);
                const status = pokemonCard.querySelector(`#status-${pokemonCard.dataset.slotId}`).value;
                const attack1 = pokemonCard.querySelector(`#attack1-${pokemonCard.dataset.slotId}`).value;
                const attack2 = pokemonCard.querySelector(`#attack2-${pokemonCard.dataset.slotId}`).value;
                const level = parseInt(pokemonCard.querySelector(`#level-${pokemonCard.dataset.slotId}`).value);

                currentTeam.push({
                    id: pokemonId,
                    hpCurrent: hpCurrent,
                    hpMax: hpMax,
                    atk: atk,
                    def: def,
                    status: status,
                    attack1: attack1,
                    attack2: attack2,
                    level: level
                });
            });
            localStorage.setItem('teamPokemon', JSON.stringify(currentTeam));

            pokedexSeen = Array.from(document.querySelectorAll('.pokedex-entry.seen')).map(entry => parseInt(entry.dataset.pokemonId));
            localStorage.setItem('pokedexSeen', JSON.stringify(pokedexSeen));
            
            localStorage.setItem('isPokedexFixed', isPokedexFixed);

            updateTrainerSummary();
        }

        // Função para carregar dados do localStorage
        function loadData() {
            const savedCharacterData = localStorage.getItem('characterData');
            if (savedCharacterData) {
                characterData = JSON.parse(savedCharacterData);
                document.getElementById('character-avatar').style.backgroundImage = `url('${characterData.avatarUrl}')`;
                document.getElementById('character-name').value = characterData.name;
                document.getElementById('money').value = characterData.money;
            }

            const savedBackpackItems = localStorage.getItem('backpackItems');
            if (savedBackpackItems) {
                const loadedItems = JSON.parse(savedBackpackItems);
                backpackItems.forEach(item => {
                    const loadedItem = loadedItems.find(loaded => loaded.name === item.name);
                    if (loadedItem) {
                        item.quantity = loadedItem.quantity;
                    }
                });
            }
            renderBackpackItems();

            const savedTeamPokemon = localStorage.getItem('teamPokemon');
            if (savedTeamPokemon) {
                teamPokemon = JSON.parse(savedTeamPokemon);
                const teamGrid = document.getElementById('team-grid');
                teamGrid.innerHTML = '';
                pokemonSlotCount = 0;

                if (teamPokemon.length > 0) {
                    teamPokemon.forEach(pkmn => {
                        addPokemonSlot(pkmn);
                    });
                } else {
                    addPokemonSlot();
                }
            } else {
                addPokemonSlot();
            }

            const savedPokedexSeen = localStorage.getItem('pokedexSeen');
            if (savedPokedexSeen) {
                pokedexSeen = JSON.parse(savedPokedexSeen);
                pokedexSeen.forEach(pokemonId => {
                    const pokedexEntryEl = document.querySelector(`.pokedex-entry[data-pokemon-id="${pokemonId}"]`);
                    if (pokedexEntryEl) {
                        pokedexEntryEl.classList.add('seen');
                    }
                });
            }
            
            const savedIsPokedexFixed = localStorage.getItem('isPokedexFixed');
            isPokedexFixed = savedIsPokedexFixed === 'true';
            
            updateTrainerSummary();
        }

        // Função para ajustar dinheiro
        function adjustMoney(amount) {
            const moneyInput = document.getElementById('money');
            let currentMoney = parseInt(moneyInput.value);
            if (isNaN(currentMoney)) {
                currentMoney = 0;
            }
            let newMoney = currentMoney + amount;
            if (newMoney < 0) {
                newMoney = 0;
            }
            moneyInput.value = newMoney;
            saveData();
        }

        // Função para renderizar itens da mochila
        function renderBackpackItems() {
            const itemList = document.getElementById('item-list');
            itemList.innerHTML = '';
            backpackItems.forEach(item => {
                const itemCard = document.createElement('div');
                itemCard.classList.add('item-card');
                itemCard.dataset.itemName = item.name;
                itemCard.title = item.name;
                itemCard.innerHTML = `
                    <img src="${item.sprite}" alt="${item.name}">
                    <p>${item.name}</p>
                    <div class="quantity-control">
                        <button class="action-button" onclick="adjustItemQuantity(this, -1)">-</button>
                        <input type="number" value="${item.quantity}" min="0" onchange="updateItemQuantity(this)">
                        <button class="action-button" onclick="adjustItemQuantity(this, 1)">+</button>
                    </div>
                `;
                itemList.appendChild(itemCard);
            });
            
            updateItemsPreview();
        }

        // Funções para ajustar quantidade de itens
        function adjustItemQuantity(button, amount) {
            const input = button.parentNode.querySelector('input');
            let currentQuantity = parseInt(input.value);
            if (isNaN(currentQuantity)) {
                currentQuantity = 0;
            }
            let newQuantity = currentQuantity + amount;
            if (newQuantity < 0) {
                newQuantity = 0;
            }
            input.value = newQuantity;
            const itemName = button.closest('.item-card').dataset.itemName;
            const itemToUpdate = backpackItems.find(item => item.name === itemName);
            if (itemToUpdate) {
                itemToUpdate.quantity = newQuantity;
            }
            saveData();
        }

        function updateItemQuantity(input) {
            let value = parseInt(input.value);
            if (isNaN(value) || value < 0) {
                value = 0;
            }
            input.value = value;
            const itemName = input.closest('.item-card').dataset.itemName;
            const itemToUpdate = backpackItems.find(item => item.name === itemName);
            if (itemToUpdate) {
                itemToUpdate.quantity = value;
            }
            saveData();
        }

        // Lista de status possíveis para Pokémon
        const pokemonStatuses = ["Normal", "Paralisado", "Envenenado", "Queimado", "Congelado", "Dormindo", "Confuso", "Enamorado", "Amedrontado", "Atraído"];

        // Função para adicionar slot de Pokémon na equipe
        function addPokemonSlot(pokemonData = null) {
            if (pokemonSlotCount >= 6) {
                alert("Sua equipe já está cheia (máximo de 6 Pokémon)!");
                return;
            }

            pokemonSlotCount++;
            const teamGrid = document.getElementById('team-grid');
            const pokemonCard = document.createElement('div');
            pokemonCard.classList.add('pokemon-card');
            pokemonCard.setAttribute('data-slot-id', pokemonSlotCount);

            let statusOptionsHtml = pokemonStatuses.map(status => `<option value="${status}">${status}</option>`).join('');

            pokemonCard.innerHTML = `
                <img src="${pokemonData && pokemonData.id ? `https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/${pokemonData.id}.png` : "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/0.png"}" alt="Selecione um Pokémon">
                <div class="info-container">
                    <div class="form-group">
                        <label for="pokemon-select-${pokemonSlotCount}">Selecione Pokémon:</label>
                        <select id="pokemon-select-${pokemonSlotCount}" onchange="updatePokemonSprite(this, ${pokemonSlotCount}); saveData()">
                            <option value="0">Selecione...</option>
                            ${pokemonList.map(p => `<option value="${p.id}">${p.name}</option>`).join('')}
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="level-${pokemonSlotCount}">Nível:</label>
                        <div class="stat-control">
                            <button class="action-button" onclick="adjustStat(this, 'level', -1); saveData()">-</button>
                            <input type="number" id="level-${pokemonSlotCount}" value="${pokemonData ? pokemonData.level : 1}" min="1" max="100" onchange="updateStat(this); saveData()">
                            <button class="action-button" onclick="adjustStat(this, 'level', 1); saveData()">+</button>
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="hp-max-${pokemonSlotCount}">HP Máximo:</label>
                        <div class="stat-control">
                            <button class="action-button" onclick="adjustStat(this, 'hp-max', -1); saveData()">-</button>
                            <input type="number" id="hp-max-${pokemonSlotCount}" value="${pokemonData ? pokemonData.hpMax : 100}" min="1" onchange="updateStat(this); saveData()">
                            <button class="action-button" onclick="adjustStat(this, 'hp-max', 1); saveData()">+</button>
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="hp-current-${pokemonSlotCount}">HP Atual:</label>
                        <div class="stat-control">
                            <button class="action-button" onclick="adjustStat(this, 'hp', -1); saveData()">-</button>
                            <input type="number" id="hp-current-${pokemonSlotCount}" value="${pokemonData ? pokemonData.hpCurrent : 100}" min="0" onchange="updateStat(this); saveData()" class="hp">
                            <button class="action-button" onclick="adjustStat(this, 'hp', 1); saveData()">+</button>
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="atk-current-${pokemonSlotCount}">ATK:</label>
                        <div class="stat-control">
                            <button class="action-button" onclick="adjustStat(this, 'atk', -1); saveData()">-</button>
                            <input type="number" id="atk-current-${pokemonSlotCount}" value="${pokemonData ? pokemonData.atk : 0}" onchange="updateStat(this); saveData()">
                            <button class="action-button" onclick="adjustStat(this, 'atk', 1); saveData()">+</button>
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="def-current-${pokemonSlotCount}">DEF:</label>
                        <div class="stat-control">
                            <button class="action-button" onclick="adjustStat(this, 'def', -1); saveData()">-</button>
                            <input type="number" id="def-current-${pokemonSlotCount}" value="${pokemonData ? pokemonData.def : 0}" onchange="updateStat(this); saveData()">
                            <button class="action-button" onclick="adjustStat(this, 'def', 1); saveData()">+</button>
                        </div>
                    </div>
                    <div class="form-group">
                        <label for="status-${pokemonSlotCount}">Status:</label>
                        <select id="status-${pokemonSlotCount}" onchange="saveData()">
                            ${statusOptionsHtml}
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="attack1-${pokemonSlotCount}">Ataque 1:</label>
                        <input type="text" id="attack1-${pokemonSlotCount}" value="${pokemonData ? pokemonData.attack1 : 'Tackle'}" onchange="saveData()">
                    </div>
                    <div class="form-group">
                        <label for="attack2-${pokemonSlotCount}">Ataque 2:</label>
                        <input type="text" id="attack2-${pokemonSlotCount}" value="${pokemonData ? pokemonData.attack2 : 'Scratch'}" onchange="saveData()">
                    </div>
                    <button class="action-button red" onclick="removePokemonSlot(this)">Remover</button>
                </div>
            `;
            teamGrid.appendChild(pokemonCard);

            if (pokemonData) {
                pokemonCard.querySelector(`#pokemon-select-${pokemonSlotCount}`).value = pokemonData.id;
                pokemonCard.querySelector(`#status-${pokemonSlotCount}`).value = pokemonData.status;
                updatePokemonSprite(pokemonCard.querySelector(`#pokemon-select-${pokemonSlotCount}`), pokemonSlotCount);
            }

            updatePokemonNameInSelect(pokemonCard.querySelector(`#pokemon-select-${pokemonSlotCount}`));
        }

        // Funções para ajustar estatísticas
        function adjustStat(button, statType, amount) {
            const input = button.parentNode.querySelector('input');
            let currentValue = parseInt(input.value);
            if (isNaN(currentValue)) {
                currentValue = 0;
            }
            let newValue = currentValue + amount;

            if (statType === 'hp') {
                if (newValue < 0) newValue = 0;
            } else if (statType === 'hp-max') {
                if (newValue < 1) newValue = 1;
            } else if (statType === 'level') {
                if (newValue < 1) newValue = 1;
                if (newValue > 100) newValue = 100;
            }
            input.value = newValue;
            saveData();
        }

        function updateStat(input) {
            let value = parseInt(input.value);
            if (isNaN(value)) {
                input.value = 0;
            } else if (input.id.startsWith('hp-') && value < 0) {
                input.value = 0;
            } else if (input.id.startsWith('level-') || input.id.startsWith('hp-max-')) {
                if (value < 1) value = 1;
                input.value = value;
            }
            saveData();
        }

        // Atualizar sprite do Pokémon
        function updatePokemonSprite(selectElement, slotId) {
            const pokemonId = selectElement.value;
            const imgElement = selectElement.closest('.pokemon-card').querySelector('img');
            if (pokemonId && pokemonId !== "0") {
                imgElement.src = `https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/versions/generation-v/black-white/animated/${pokemonId}.gif`;
                imgElement.onerror = () => {
                    imgElement.src = `https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/${pokemonId}.png`;
                    imgElement.onerror = null;
                };
            } else {
                imgElement.src = "https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/0.png";
            }
        }

        // Remover slot de Pokémon
        function removePokemonSlot(button) {
            const pokemonCard = button.closest('.pokemon-card');
            pokemonCard.remove();
            pokemonSlotCount--;
            saveData();
        }

        // Atualizar nomes de Pokémon na lista
        async function updatePokemonNameInSelect(selectElement) {
            const currentSelectedValue = selectElement.value;
            selectElement.innerHTML = '<option value="0">Selecione...</option>';

            const validPokemonList = pokemonList.filter(p => p.id > 0);

            for (const p of validPokemonList) {
                const option = document.createElement('option');
                option.value = p.id;

                try {
                    const response = await fetch(`https://pokeapi.co/api/v2/pokemon-species/${p.id}/`);
                    const data = await response.json();
                    const pokemonName = data.names.find(name => name.language.name === 'en')?.name || data.name;
                    option.textContent = `#${String(p.id).padStart(3, '0')} - ${pokemonName.charAt(0).toUpperCase() + pokemonName.slice(1)}`;
                } catch (error) {
                    console.error(`Erro ao buscar nome do Pokémon ${p.id}:`, error);
                    option.textContent = `#${String(p.id).padStart(3, '0')} - Erro`;
                }
                selectElement.appendChild(option);
            }

            if (currentSelectedValue && selectElement.querySelector(`option[value="${currentSelectedValue}"]`)) {
                selectElement.value = currentSelectedValue;
            }
        }

        // Renderizar Pokédex
        function renderPokedex() {
            const pokedexGrid = document.getElementById('pokedex-grid');
            pokedexGrid.innerHTML = '';
            pokemonList.forEach(pokemon => {
                const pokedexEntry = document.createElement('div');
                pokedexEntry.classList.add('pokedex-entry');
                pokedexEntry.setAttribute('data-pokemon-id', pokemon.id);
                pokedexEntry.id = `pokedex-entry-${pokemon.id}`;
                
                if (pokedexSeen.includes(pokemon.id)) {
                    pokedexEntry.classList.add('seen');
                }

                const spriteUrl = `https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/${pokemon.id}.png`;
                pokedexEntry.innerHTML = `
                    <img src="${spriteUrl}" alt="Pokémon #${pokemon.id}">
                    <div class="pokemon-name-hover">Carregando...</div>
                `;
                pokedexGrid.appendChild(pokedexEntry);

                fetch(`https://pokeapi.co/api/v2/pokemon-species/${pokemon.id}/`)
                    .then(response => response.json())
                    .then(data => {
                        const pokemonName = data.names.find(name => name.language.name === 'en')?.name || data.name;
                        pokedexEntry.querySelector('.pokemon-name-hover').textContent = `#${String(pokemon.id).padStart(3, '0')} ${pokemonName.charAt(0).toUpperCase() + pokemonName.slice(1)}`;
                    })
                    .catch(error => {
                        console.error(`Erro ao buscar nome do Pokémon ${pokemon.id}:`, error);
                        pokedexEntry.querySelector('.pokemon-name-hover').textContent = `#${String(pokemon.id).padStart(3, '0')} (Erro)`;
                    });

                pokedexEntry.addEventListener('click', () => {
                    document.querySelectorAll('.pokedex-entry').forEach(entry => {
                        entry.classList.remove('selected');
                    });
                    pokedexEntry.classList.add('selected');
                    showPokemonDetails(pokemon.id);
                });
            });
        }
        
        // Filtrar Pokédex
        function filterPokedex(searchTerm) {
            const normalizedTerm = searchTerm.toLowerCase().trim();
            document.querySelectorAll('.pokedex-entry').forEach(entry => {
                const pokemonId = entry.dataset.pokemonId;
                const nameElement = entry.querySelector('.pokemon-name-hover');
                const name = nameElement.textContent.toLowerCase();
                
                if (name.includes(normalizedTerm) || pokemonId.toString().includes(normalizedTerm)) {
                    entry.style.display = 'flex';
                } else {
                    entry.style.display = 'none';
                }
            });
        }
        
        // Mostrar detalhes do Pokémon
        async function showPokemonDetails(pokemonId) {
            const pokedexDetails = document.getElementById('pokedex-details');
            pokedexDetails.classList.add('active');
            pokedexDetails.innerHTML = '<div class="loading-message">Carregando detalhes...</div>';
            
            try {
                const response = await fetch(`https://pokeapi.co/api/v2/pokemon/${pokemonId}/`);
                const data = await response.json();
                
                const name = data.name.charAt(0).toUpperCase() + data.name.slice(1);
                const id = data.id;
                const types = data.types.map(t => t.type.name);
                const stats = data.stats.map(s => ({
                    name: s.stat.name,
                    value: s.base_stat
                }));
                
                const isSeen = pokedexSeen.includes(pokemonId);
                
                let detailsHTML = `
                    <div class="pin-button-container">
                        <div class="pin-button ${isPokedexFixed ? 'fixed' : ''}" id="pin-pokedex" title="${isPokedexFixed ? 'Desfixar painel' : 'Fixar painel'}">
                            📌
                        </div>
                    </div>
                    <div class="pokemon-details">
                        <div class="pokemon-details-header">
                            <div class="pokemon-details-image">
                                <img src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/${pokemonId}.png" alt="${name}">
                            </div>
                            <div class="pokemon-details-info">
                                <div class="pokemon-details-name">#${String(id).padStart(3, '0')} ${name}</div>
                                <div class="pokemon-details-types">
                `;
                
                types.forEach(type => {
                    const typeName = type.charAt(0).toUpperCase() + type.slice(1);
                    detailsHTML += `<span class="pokemon-type" style="background-color: ${getTypeColor(type)};">${typeName}</span>`;
                });
                
                detailsHTML += `
                                </div>
                            </div>
                        </div>
                        <div class="pokemon-stats">
                            <h3>Status Base</h3>
                `;
                
                stats.forEach(stat => {
                    const statName = getStatName(stat.name);
                    const statValue = stat.value;
                    const barWidth = Math.min(100, (statValue / 255) * 100);
                    
                    detailsHTML += `
                        <div class="stat-row">
                            <div class="stat-name">${statName}</div>
                            <div class="stat-bar-container">
                                <div class="stat-bar" style="width: ${barWidth}%;"></div>
                            </div>
                            <div class="stat-value">${statValue}</div>
                        </div>
                    `;
                });
                
                detailsHTML += `
                        </div>
                        <div class="seen-toggle">
                            <button class="action-button ${isSeen ? 'red' : ''}" onclick="toggleSeenStatus(${pokemonId}, this)">
                                ${isSeen ? 'Marcar como Desvisto' : 'Marcar como Visto'}
                            </button>
                        </div>
                        <div class="pokemon-moves">
                            <h3>Movimentos (Platinum)</h3>
                            <div id="pokemon-moves-container" class="moves-loading">
                                Carregando movimentos...
                            </div>
                        </div>
                    </div>
                `;
                
                pokedexDetails.innerHTML = detailsHTML;
                
                // Carrega os movimentos do Pokémon Platinum
                loadPokemonMoves(pokemonId);
                
                const pinButton = document.getElementById('pin-pokedex');
                if (pinButton) {
                    pinButton.addEventListener('click', function(e) {
                        e.stopPropagation();
                        togglePinPokedex();
                    });
                }
                
                if (isPokedexFixed) {
                    pokedexDetails.classList.add('fixed');
                }
                
            } catch (error) {
                console.error(`Erro ao buscar detalhes do Pokémon ${pokemonId}:`, error);
                pokedexDetails.innerHTML = '<div class="loading-message">Erro ao carregar detalhes do Pokémon.</div>';
            }
        }
        
        // Carregar movimentos do Pokémon
        async function loadPokemonMoves(pokemonId) {
            try {
                const movesContainer = document.getElementById('pokemon-moves-container');
                movesContainer.innerHTML = '<div class="moves-loading">Carregando movimentos...</div>';
                
                // Busca os dados de movimentos do Pokémon na versão Platinum
                const response = await fetch(`https://pokeapi.co/api/v2/pokemon/${pokemonId}/`);
                const pokemonData = await response.json();
                
                // Encontra a versão Platinum nos dados de movimentos
                let platinumMoves = [];
                
                // Verifica se há dados de movimentos por nível
                if (pokemonData.moves) {
                    for (const moveData of pokemonData.moves) {
                        // Encontra os detalhes da versão Platinum
                        const versionGroupDetails = moveData.version_group_details.find(
                            vgd => vgd.version_group.name === 'platinum'
                        );
                        
                        if (versionGroupDetails) {
                            // Busca os detalhes completos do movimento
                            const moveResponse = await fetch(moveData.move.url);
                            const moveDetails = await moveResponse.json();
                            
                            // Obtém o nome em português do movimento
                            const moveNamePT = moveDetails.names.find(n => n.language.name === 'pt')?.name || 
                                              moveDetails.names.find(n => n.language.name === 'en')?.name || 
                                              moveDetails.name;
                            
                            // Adiciona à lista de movimentos
                            platinumMoves.push({
                                name: moveNamePT,
                                level: versionGroupDetails.level_learned_at,
                                method: versionGroupDetails.move_learn_method.name,
                                type: moveDetails.type.name,
                                power: moveDetails.power,
                                accuracy: moveDetails.accuracy,
                                pp: moveDetails.pp
                            });
                        }
                    }
                }
                
                // Ordena os movimentos por nível
                platinumMoves.sort((a, b) => a.level - b.level);
                
                // Renderiza a tabela de movimentos
                if (platinumMoves.length > 0) {
                    let movesHTML = `
                        <table class="moves-table">
                            <thead>
                                <tr>
                                    <th>Movimento</th>
                                    <th>Tipo</th>
                                    <th>Nível</th>
                                    <th>Método</th>
                                    <th>Poder</th>
                                    <th>Precisão</th>
                                    <th>PP</th>
                                </tr>
                            </thead>
                            <tbody>
                    `;
                    
                    platinumMoves.forEach(move => {
                        movesHTML += `
                            <tr>
                                <td class="move-name">${move.name}</td>
                                <td><span class="move-type" style="background-color: ${getTypeColor(move.type)};">${move.type.charAt(0).toUpperCase() + move.type.slice(1)}</span></td>
                                <td class="move-level">${move.level > 0 ? move.level : '-'}</td>
                                <td class="move-method">${getMoveMethodName(move.method)}</td>
                                <td class="move-power">${move.power || '-'}</td>
                                <td class="move-accuracy">${move.accuracy ? move.accuracy + '%' : '-'}</td>
                                <td class="move-pp">${move.pp}</td>
                            </tr>
                        `;
                    });
                    
                    movesHTML += `
                            </tbody>
                        </table>
                    `;
                    
                    movesContainer.innerHTML = movesHTML;
                } else {
                    movesContainer.innerHTML = '<div class="moves-loading">Nenhum movimento encontrado para o Pokémon Platinum.</div>';
                }
            } catch (error) {
                console.error(`Erro ao carregar movimentos do Pokémon ${pokemonId}:`, error);
                document.getElementById('pokemon-moves-container').innerHTML = '<div class="moves-loading">Erro ao carregar movimentos.</div>';
            }
        }
        
        // Obter nome do método de aprendizado
        function getMoveMethodName(method) {
            const methodNames = {
                'level-up': 'Nível',
                'egg': 'Ovo',
                'tutor': 'Tutor',
                'machine': 'MT/MO',
                'stadium-surfing-pikachu': 'Surf Pikachu',
                'light-ball-egg': 'Ovo (Light Ball)',
                'colosseum-purification': 'Purificação',
                'xd-shadow': 'XD Shadow',
                'xd-purification': 'XD Purification',
                'form-change': 'Mudança de Forma'
            };
            return methodNames[method] || method;
        }
        
        // Fixar/desfixar Pokédex
        function togglePinPokedex() {
            isPokedexFixed = !isPokedexFixed;
            const pinButton = document.getElementById('pin-pokedex');
            
            if (isPokedexFixed) {
                document.getElementById('pokedex-details').classList.add('fixed');
                if (pinButton) {
                    pinButton.classList.add('fixed');
                    pinButton.title = 'Desfixar painel';
                }
            } else {
                document.getElementById('pokedex-details').classList.remove('fixed');
                if (pinButton) {
                    pinButton.classList.remove('fixed');
                    pinButton.title = 'Fixar painel';
                }
            }
            
            saveData();
        }
        
        // Alternar status "visto" do Pokémon
        function toggleSeenStatus(pokemonId, button) {
            const index = pokedexSeen.indexOf(pokemonId);
            const isSeen = index !== -1;
            
            if (isSeen) {
                pokedexSeen.splice(index, 1);
                button.textContent = 'Marcar como Visto';
                button.classList.remove('red');
            } else {
                pokedexSeen.push(pokemonId);
                button.textContent = 'Marcar como Desvisto';
                button.classList.add('red');
            }
            
            const entry = document.querySelector(`.pokedex-entry[data-pokemon-id="${pokemonId}"]`);
            if (entry) {
                entry.classList.toggle('seen', !isSeen);
            }
            
            updatePokedexSummary();
            saveData();
        }
        
        // Obter cor do tipo
        function getTypeColor(type) {
            const typeColors = {
                normal: '#A8A878',
                fire: '#F08030',
                water: '#6890F0',
                electric: '#F8D030',
                grass: '#78C850',
                ice: '#98D8D8',
                fighting: '#C03028',
                poison: '#A040A0',
                ground: '#E0C068',
                flying: '#A890F0',
                psychic: '#F85888',
                bug: '#A8B820',
                rock: '#B8A038',
                ghost: '#705898',
                dragon: '#7038F8',
                dark: '#705848',
                steel: '#B8B8D0',
                fairy: '#EE99AC'
            };
            return typeColors[type] || '#777';
        }
        
        // Obter nome da estatística
        function getStatName(stat) {
            const statNames = {
                'hp': 'HP',
                'attack': 'Ataque',
                'defense': 'Defesa',
                'special-attack': 'Ataque Especial',
                'special-defense': 'Defesa Especial',
                'speed': 'Velocidade'
            };
            return statNames[stat] || stat;
        }
        
        // Atualizar resumo do treinador
        function updateTrainerSummary() {
            updateTeamPreview();
            updatePokedexSummary();
            updateItemsPreview();
        }
        
        // Atualizar pré-visualização da equipe
        function updateTeamPreview() {
            const teamPreview = document.getElementById('team-preview');
            teamPreview.innerHTML = '';
            
            const team = [];
            document.querySelectorAll('#team-grid .pokemon-card').forEach(pokemonCard => {
                const pokemonId = pokemonCard.querySelector('select').value;
                const hpCurrent = parseInt(pokemonCard.querySelector(`#hp-current-${pokemonCard.dataset.slotId}`).value);
                const hpMax = parseInt(pokemonCard.querySelector(`#hp-max-${pokemonCard.dataset.slotId}`).value);
                const status = pokemonCard.querySelector(`#status-${pokemonCard.dataset.slotId}`).value;
                const level = parseInt(pokemonCard.querySelector(`#level-${pokemonCard.dataset.slotId}`).value);
                
                if (pokemonId && pokemonId !== "0") {
                    team.push({
                        id: pokemonId,
                        hpCurrent: hpCurrent,
                        hpMax: hpMax,
                        status: status,
                        level: level
                    });
                }
            });
            
            for (let i = 0; i < 6; i++) {
                const slot = document.createElement('div');
                slot.classList.add('team-slot');
if (i < team.length) {
                    const pokemon = team[i];
                    const hpPercentage = Math.min(100, (pokemon.hpCurrent / pokemon.hpMax) * 100);
                    
                    slot.innerHTML = `
                        <img src="https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/${pokemon.id}.png" alt="Pokémon #${pokemon.id}">
                        <div class="hp-bar-container">
                            <div class="hp-bar" style="width: ${hpPercentage}%; background-color: ${getHpBarColor(hpPercentage)};"></div>
                        </div>
                        <div class="hp-info">HP: ${pokemon.hpCurrent}/${pokemon.hpMax}</div>
                        <div class="level-info">Lv. ${pokemon.level}</div>
                    `;
                } else {
                    slot.innerHTML = '&nbsp;';
                }
                
                teamPreview.appendChild(slot);
            }
        }
        
        // Obter cor da barra de HP
        function getHpBarColor(hpPercentage) {
            if (hpPercentage >= 70) return '#4caf50';
            if (hpPercentage >= 30) return '#ffc107';
            return '#f44336';
        }
        
        // Atualizar resumo da Pokédex
        function updatePokedexSummary() {
            const summary = document.getElementById('pokedex-summary');
            summary.textContent = `Pokédex: ${pokedexSeen.length}/493`;
        }
        
        // Atualizar pré-visualização de itens
        function updateItemsPreview() {
            const itemsPreview = document.getElementById('items-preview');
            itemsPreview.innerHTML = '';
            
            const itemsWithQuantity = backpackItems.filter(item => item.quantity > 0);
            const itemsToShow = itemsWithQuantity.slice(0, 5);
            
            itemsToShow.forEach(item => {
                const itemDiv = document.createElement('div');
                itemDiv.classList.add('item-preview');
                itemDiv.title = item.name;
                itemDiv.innerHTML = `
                    <img src="${item.sprite}" alt="${item.name}">
                    <span class="item-quantity">${item.quantity}</span>
                `;
                itemsPreview.appendChild(itemDiv);
            });
            
            if (itemsToShow.length === 0) {
                itemsPreview.innerHTML = '<div style="font-size:0.7em;">Nenhum item na mochila</div>';
            } else if (itemsWithQuantity.length > 5) {
                const moreItems = document.createElement('div');
                moreItems.textContent = `+${itemsWithQuantity.length - 5} itens`;
                moreItems.style.fontSize = '0.7em';
                moreItems.style.marginLeft = '5px';
                itemsPreview.appendChild(moreItems);
            }
        }
        
        // Renderizar aba de ataques
        function renderAttacksTab() {
            const attacksContainer = document.getElementById('attacks-container');
            attacksContainer.innerHTML = '';
            
            const attacksByType = {};
            attackData.forEach(attack => {
                if (!attacksByType[attack.type]) {
                    attacksByType[attack.type] = [];
                }
                attacksByType[attack.type].push(attack);
            });
            
            for (const type in attacksByType) {
                const section = document.createElement('div');
                section.classList.add('attack-type-section');
                
                const header = document.createElement('h3');
                header.textContent = `Ataques de ${type}`;
                section.appendChild(header);
                
                const table = document.createElement('table');
                table.classList.add('attack-table');
                
                const thead = document.createElement('thead');
                thead.innerHTML = `
                    <tr>
                        <th>Movimento</th>
                        <th>Ativação</th>
                        <th>Efeito</th>
                    </tr>
                `;
                table.appendChild(thead);
                
                const tbody = document.createElement('tbody');
                attacksByType[type].forEach(attack => {
                    const row = document.createElement('tr');
                    row.innerHTML = `
                        <td class="attack-name">${attack.name}</td>
                        <td class="attack-activation">${attack.activation}</td>
                        <td class="attack-effect">${attack.effect}</td>
                    `;
                    tbody.appendChild(row);
                });
                table.appendChild(tbody);
                
                section.appendChild(table);
                attacksContainer.appendChild(section);
            }
        }
        
        // Filtrar lista de Pokémon
        function filterPokemonList() {
            const searchTerm = document.getElementById('pokemon-search').value.toLowerCase();
            document.querySelectorAll('#team-grid select').forEach(select => {
                Array.from(select.options).forEach(option => {
                    const pokemonName = option.textContent.toLowerCase();
                    option.style.display = pokemonName.includes(searchTerm) ? 'block' : 'none';
                });
            });
        }

        // Configurar abas
        function setupTabs() {
            const tabs = [
                { id: 'character', button: document.querySelector('[data-tab="character"]') },
                { id: 'backpack', button: document.querySelector('[data-tab="backpack"]') },
                { id: 'team', button: document.querySelector('[data-tab="team"]') },
                { id: 'pokedex', button: document.querySelector('[data-tab="pokedex"]') },
                { id: 'attacks', button: document.querySelector('[data-tab="attacks"]') }
            ];

            tabs.forEach(tab => {
                tab.button.addEventListener('click', () => {
                    tabs.forEach(t => {
                        t.button.classList.remove('active');
                        document.getElementById(t.id).classList.remove('active');
                    });
                    tab.button.classList.add('active');
                    document.getElementById(tab.id).classList.add('active');
                    saveData();
                });
            });
        }

        // Configurar evento de alteração de avatar
        function setupAvatarChange() {
            const avatarFileInput = document.getElementById('avatar-file');
            const characterAvatar = document.getElementById('character-avatar');

            avatarFileInput.addEventListener('change', function() {const file = this.files && this.files.length > 0 ? this.files[0] : null;
                if (file) {
                    const reader = new FileReader();
                    reader.onload = function(e) {
                        characterAvatar.style.backgroundImage = `url('${e.target.result}')`;
                        saveData();
                    };
                    reader.readAsDataURL(file);
                } else {
                    characterAvatar.style.backgroundImage = 'none';
                    saveData();
                }
            });
        }

        // Inicializar aplicação
        function initApp() {
            setupTabs();
            setupAvatarChange();
            renderBackpackItems();
            renderPokedex();
            renderAttacksTab();
            loadData();
        }

        // Iniciar quando o documento estiver pronto
        document.addEventListener('DOMContentLoaded', initApp);
    
// Modal completo com ficha do Pokémon
document.getElementById("team-preview").addEventListener("click", function (e) {
    const slot = e.target.closest(".team-slot");
    if (!slot) return;

    const index = Array.from(slot.parentNode.children).indexOf(slot);
    const teamCards = document.querySelectorAll("#team-grid .pokemon-card");

    if (index >= teamCards.length) return;

    const card = teamCards[index];
    const id = card.querySelector("select").value;
    const name = card.querySelector("select").options[card.querySelector("select").selectedIndex].textContent;
    const atk1 = card.querySelector(`#attack1-${card.dataset.slotId}`)?.value || "---";
    const atk2 = card.querySelector(`#attack2-${card.dataset.slotId}`)?.value || "---";
    const level = card.querySelector(`#level-${card.dataset.slotId}`)?.value || "--";
    const hpMax = parseInt(card.querySelector(`#hp-max-${card.dataset.slotId}`)?.value) || 1;
    const hpNow = parseInt(card.querySelector(`#hp-current-${card.dataset.slotId}`)?.value) || 0;
    const atk = card.querySelector(`#atk-current-${card.dataset.slotId}`)?.value || "--";
    const def = card.querySelector(`#def-current-${card.dataset.slotId}`)?.value || "--";
    const status = card.querySelector(`#status-${card.dataset.slotId}`)?.value || "--";

    const hpPercent = Math.min(100, (hpNow / hpMax) * 100);
    let hpColor = '#4caf50';
    if (hpPercent < 30) hpColor = '#f44336';
    else if (hpPercent < 70) hpColor = '#ffc107';

    document.getElementById("modalTitle").textContent = name;
    document.getElementById("modalLevel").textContent = level;
    document.getElementById("modalHP").textContent = `${hpNow}/${hpMax}`;
    document.getElementById("modalHPBar").style.width = hpPercent + "%";
    document.getElementById("modalHPBar").style.backgroundColor = hpColor;
    document.getElementById("modalATK").textContent = atk;
    document.getElementById("modalDEF").textContent = def;
    document.getElementById("modalStatus").textContent = status;
    document.getElementById("modalAttack1").textContent = atk1;
    document.getElementById("modalAttack2").textContent = atk2;
    document.getElementById("modalSprite").style.backgroundImage = `url(https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/${id}.png)`;
    
    document.getElementById("pokemonModal").style.display = "flex";
});

function closePokemonModal() {
    document.getElementById("pokemonModal").style.display = "none";
}
document.getElementById("team-preview").addEventListener("click", function (e) {
    const slot = e.target.closest(".team-slot");
    if (!slot) return;

    const index = Array.from(slot.parentNode.children).indexOf(slot);
    const teamCards = document.querySelectorAll("#team-grid .pokemon-card");

    if (index >= teamCards.length) return;

    const card = teamCards[index];
    const select = card.querySelector("select");
    const name = select.options[select.selectedIndex].textContent || "Pokémon";
    const atk1 = card.querySelector(`#attack1-${card.dataset.slotId}`)?.value || "---";
    const atk2 = card.querySelector(`#attack2-${card.dataset.slotId}`)?.value || "---";

    document.getElementById("modalTitle").textContent = name;
    document.getElementById("modalAttack1").textContent = atk1;
    document.getElementById("modalAttack2").textContent = atk2;
    document.getElementById("pokemonModal").style.display = "flex";
});

function closePokemonModal() {
    document.getElementById("pokemonModal").style.display = "none";
}

</script>


<!-- Modal completo da ficha do Pokémon -->
<div id="pokemonModal" class="modal" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%; background-color: rgba(0,0,0,0.6); justify-content:center; align-items:center; z-index:10000;">
  <div style="background:#fff; border:4px solid #222; border-radius:8px; padding:20px; max-width:320px; font-family: 'Press Start 2P', cursive; font-size: 0.5em; text-align:center;">
    <div id="modalSprite" style="width:96px;height:96px;margin:auto;background-size:contain;background-repeat:no-repeat;background-position:center;"></div>
    <h3 id="modalTitle">Pokémon</h3>
    <p><strong>Nível:</strong> <span id="modalLevel">--</span></p>
    <p><strong>HP:</strong> <span id="modalHP">--</span></p>
    <div style="width:80%;height:8px;background:#ccc;margin:5px auto;border-radius:4px;">
      <div id="modalHPBar" style="height:100%;width:0%;background:#4caf50;"></div>
    </div>
    <p><strong>ATK:</strong> <span id="modalATK">--</span> | <strong>DEF:</strong> <span id="modalDEF">--</span></p>
    <p><strong>Status:</strong> <span id="modalStatus">--</span></p>
    <p><strong>Ataque 1:</strong> <span id="modalAttack1">---</span></p>
    <p><strong>Ataque 2:</strong> <span id="modalAttack2">---</span></p>
    <button onclick="closePokemonModal()" class="action-button red" style="margin-top:10px;">Fechar</button>
  </div>
</div>

<div id="pokemonModal" class="modal" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%; background-color: rgba(0,0,0,0.6); justify-content:center; align-items:center; z-index:10000;">
  <div style="background:#fff; border:4px solid #222; border-radius:8px; padding:20px; max-width:300px; font-family: 'Press Start 2P', cursive; font-size: 0.55em; text-align:center;">
    <h3 id="modalTitle">Pokémon</h3>
    <p><strong>Ataque 1:</strong> <span id="modalAttack1">---</span></p>
    <p><strong>Ataque 2:</strong> <span id="modalAttack2">---</span></p>
    <button onclick="closePokemonModal()" class="action-button red" style="margin-top:10px;">Fechar</button>
  </div>
</div>

</body>
</html>

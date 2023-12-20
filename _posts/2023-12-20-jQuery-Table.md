<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0">
    <link rel="stylesheet" type="text/css" href="https://cdn.datatables.net/1.13.4/css/jquery.dataTables.min.css">
    <script type="text/javascript" language="javascript" src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script>var define = null;</script>
    <script type="text/javascript" language="javascript" src="https://cdn.datatables.net/1.13.4/js/jquery.dataTables.min.js"></script>
</head>
<body>
<div id="table"></div>
<label for="nameInput">Name:</label>
<input type="text" id="nameInput">
<label for="typeInput">Type:</label>
<input type="text" id="typeInput">
<label for="levelInput">Level:</label>
<input type="number" id="levelInput">
<label for="personalityInput">Personality:</label>
<input type="text" id="personalityInput">
<button id="add-row-btn">Add Row</button>
<script>
    function getAPI() {
        return [
            { name: 'Pikachu', type: 'Electric', level: 25, personality: 'Cheerful' },
            { name: 'Bulbasaur', type: 'Grass/Poison', level: 20, personality: 'Brave' },
            { name: 'Charlizard', type: 'Fire/Flying', level: 36, personality: 'Quiet' },
            { name: 'Squirtle', type: 'Water', level: 22, personality: 'Modest' },
            { name: 'Snivy', type: 'Grass', level: 17, personality: 'Mild' },
            { name: 'Tepig', type: 'Fire', level: 12, personality: 'Serious' },
            { name: 'Oshawott', type: 'Water', level: 19, personality: 'Quiet' },
            { name: 'Zorua', type: 'Dark', level: 14, personality: 'Docile' },
            { name: 'Dragonite', type: 'Dragon/Flying', level: 44, personality: 'Brave' },
            { name: 'Zekrom', type: 'Dragon/Electric', level: 50, personality: 'Rash' },
            { name: 'Mudkip', type: 'Water', level: 2, personality: 'Lonely' },
            { name: 'Torchic', type: 'Fire', level: 16, personality: 'Rash' },
            { name: 'Treecko', type: 'Grass', level: 12, personality: 'Quiet' },
            { name: 'Eevee', type: 'Normal', level: 18, personality: 'Timid' },
            { name: 'Chespin', type: 'Grass', level: 8, personality: 'Mild' },
            { name: 'Fennekin', type: 'Fire', level: 6, personality: 'Timid' },
            { name: 'Froakie', type: 'Water', level: 7, personality: 'Modest' },
        ];
    }
    function addRow(table) {
        table.row.add([
            $('#nameInput').val(),
            $('#typeInput').val(),
            $('#levelInput').val(),
            $('#personalityInput').val(),
            '<button class="remove-btn">Remove</button> <button class="update-btn">Update</button>'
        ]).draw();
    }
    function updateRow(table, rowIndex) {
        table.row(rowIndex).data([
            $('#nameInput').val(),
            $('#typeInput').val(),
            $('#levelInput').val(),
            $('#personalityInput').val(),
            '<button class="remove-btn">Remove</button> <button class="update-btn">Update</button>'
        ]).draw();
    }
    $(document).ready(function() {
        var pokemons = getAPI();

        var table = $("<table>").attr("id", "test").addClass("table");
        var thead = $("<thead>").appendTo(table);
        var tbody = $("<tbody>").appendTo(table);

        var headerRow = $("<tr>").appendTo(thead);
        $("<th>").text("Name").appendTo(headerRow);
        $("<th>").text("Type").appendTo(headerRow);
        $("<th>").text("Level").appendTo(headerRow);
        $("<th>").text("Personality").appendTo(headerRow);
        $("<th>").text("Actions").appendTo(headerRow);

        pokemons.forEach(function(pokemon) {
            var row = $("<tr>").appendTo(tbody);
            $("<td>").text(pokemon.name).appendTo(row);
            $("<td>").text(pokemon.type).appendTo(row);
            $("<td>").text(pokemon.level).appendTo(row);
            $("<td>").text(pokemon.personality).appendTo(row);
            $("<td>").html('<button class="remove-btn">Remove</button> <button class="update-btn">Update</button>').appendTo(row);
        });

        table.appendTo("#table");
        var test = $("#test").DataTable();

        $('#test tbody').on('click', ".remove-btn", function () {
            console.log("running");
            test.row($(this).parents('tr')).remove().draw();
        });

        $('#test tbody').on('click', ".update-btn", function () {
            var rowIndex = test.row($(this).parents('tr')).index();
            updateRow(test, rowIndex);
        });

        $("#add-row-btn").on("click", function() {
            addRow(test);
        });
    });
</script>
</body>
</html>

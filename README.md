# DatePicker-Compares
#We need to compate 2 dates then use this code 
```
  @*<script src="https://code.jquery.com/jquery-3.3.1.min.js"></script>*@
    @*<script src="https://unpkg.com/gijgo@1.9.13/js/gijgo.min.js" type="text/javascript"></script>*@

    <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.6/jquery.min.js" type="text/javascript"></script>
    <script src="http://ajax.googleapis.com/ajax/libs/jqueryui/1.8/jquery-ui.min.js"
            type="text/javascript"></script>
    <link href="http://ajax.googleapis.com/ajax/libs/jqueryui/1.8/themes/start/jquery-ui.css"
          rel="Stylesheet" type="text/css" />
    <script type="text/javascript">
        $(function () {
            $("#startDate").datepicker({
                numberOfMonths: 2,
                onSelect: function (selected) {
                    var dt = new Date(selected);
                    dt.setDate(dt.getDate() + 1);
                    $("#endDate").datepicker("option", "minDate", dt);
                }
            });
            $("#endDate").datepicker({
                numberOfMonths: 2,
                onSelect: function (selected) {
                    var dt = new Date(selected);
                    dt.setDate(dt.getDate() - 1);
                    $("#startDate").datepicker("option", "maxDate", dt);
                }
            });
        });
    </script>
    ```

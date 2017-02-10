# datatables-slimscroll
beautify the datatables dot net table scrollbar using slimscroll
<pre>
//initialise the table like below
$(document).ready(function() {
	//initialise the table :
    $('#example').DataTable({
    	scrollY:        '50vh',
        scrollCollapse: true,
        paging:         false,
        "fnDrawCallback": function (oSettings) {
	     	$('.dataTables_scrollBody').slimScroll({
	        height: '150px'
	     });
	}
	
});
//redraw the datatable once again so that it will adjust the datatable to fit the slimscroll properly.
$('#example').DataTable().draw();
</pre>

# Shrutikulkarni_Question2
program of finding longest strings
<script>
// Javascript program to find longest common prefix
	
	function longestCommonPrefix(a)
	{
		let size = a.length;
		if (size == 0)
			return "";

		if (size == 1)
			return a[0];

		
		a.sort();

		
		let end = Math.min(a[0].length, a[size-1].length);

		/* find the common prefix between the first and
		last string */
		let i = 0;
		while (i < end && a[0][i] == a[size-1][i] )
			i++;

		let pre = a[0].substring(0, i);
		return pre;
	}
	
	/* Driver Function to test other function */
	let input=["VLiNKEDTECH", "VLiSer", "VLiedTevices"];
	document.write( "The longest Common Prefix is : " +
								longestCommonPrefix(input));
	

</script>



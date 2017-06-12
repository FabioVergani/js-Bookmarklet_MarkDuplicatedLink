# js-Bookmarklet_MarkDuplicatedLink

(function(w){
	const d=w.document, B=[], m=[];
	let a=d.getElementsByTagName('a');
	for(let x of a){let i=x.href;(m.includes(i)?B:m).push(i)};
	if(B.length){
	 a=d.querySelectorAll('[href="'+B.join('"],[href="')+'"]');
	 for(let x of a){
		x=x.style;
		x.background='red';
		x.border='3px dashed #68c200';
		x.display='inline-block';
	 }
	}
})(window);

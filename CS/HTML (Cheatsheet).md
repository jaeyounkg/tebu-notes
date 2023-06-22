# Basic Elements

## Span

```html
<span style="color:#ff0000;font-weight:bold;">キーワード</span>
```

## Tables

```html
<table>
	<thead>
		<tr> <!-- table row -->
			<th>Name</th> <!-- table header -->
			<th>Price</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<th colSpan="2">Category</th>
		</tr>
		<tr>
			<td>Apple</td> <!-- table data -->
			<td>$1</td>
		</tr>
	</tbody>
</table>
```

## Lists

```html
<ul> <!-- unordered list -->
  <li>1つめの項目</li>
  <li>2つめの項目</li>
</ul>

<ol> <!-- ordered list -->
  <li>1つめの項目</li>
  <li>2つめの項目</li>
</ol>
```

## Forms

```html
<form>
	<input type="text" placeholder="Search..." />
	<label>
		<input type="checkbox" /> Only show products in stock
	</label>
</form>
```
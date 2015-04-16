# wpfSnippet
-----------------------------------
Coleção de Snippets e métodos ágeis para melhor produtividade no desenvolvimento em Windows Presentation Foundation, através de Visual Studio + [ReSharper](https://www.jetbrains.com/resharper/download/).  
Digite o comando, aperte TAB e veja a mágica acontecer. :rocket:

### Getting Started
------------------

- [Baixe](https://github.com/dotpegaso/wpfsnippet/archive/master.zip) o arquivo e entre na pasta *Snippets*
- Abra o `Visual Studio` e, em seu menu superior, navegue até `Resharper > Tools > Templates Explorer`
- Em `Scopes` selecione `Global`, clique em `Import` e adicione os snippets ao seu ReSharper

![alt tag](http://s18.postimg.org/bf2bzy8op/example.gif)


### Estrutura Básica de Grids
------------------
Os comandos abaixo faciltam a construção de markdown para criação de grids e suas propriedades.
Para decorar os comandos, lembre-se das iniciais maiúsculas que vão após o início da marcação.

![alt tag](http://s28.postimg.org/oofm0d4bh/estruturabasica.gif)

**grid**
~~~~~xml
<Grid Margin="5">

	<!-- Quantidade de colunas -->
	<Grid.ColumnDefinitions>
		<ColumnDefinition Width="Auto" />
		...
	</Grid.ColumnDefinitions>

	<!-- Quantidade de linhas -->
	<Grid.RowDefinitions>
		<RowDefinition Height="Auto" />
		...
	</Grid.RowDefinitions>

	<!-- Código -->
	...

</Grid>
~~~~~

**gridcd**
~~~~~xml
<Grid.ColumnDefinitions>
    <ColumnDefinition Width="Auto" />
</Grid.ColumnDefinitions>
~~~~~

**cold**
~~~~~xml
<ColumnDefinition Width="Auto" />
~~~~~

**gridc**
~~~~~xml
<Grid Grid.Column="0" Margin="5">
...
</Grid>
~~~~~

**gridrd**
~~~~~xml
<Grid.RowDefinitions>
    <RowDefinition Height="Auto" />
</Grid.RowDefinitions>
~~~~~

**rowd**
~~~~~xml
<RowDefinition Height="Auto" />
~~~~~

**gridr**
~~~~~xml
<Grid Grid.Row="0" Margin="5">
...
</Grid>
~~~~~

**gridrc**
~~~~~xml
<Grid Grid.Row="0" Grid.Column="0" Margin="5">
...
</Grid>
~~~~~

**gridcr**
~~~~~xml
<Grid Grid.Column="0" Grid.Row="0" Margin="5">
...
</Grid>
~~~~~

### Elementos
------------------
Comandos para adicionar elementos básicos já preenchidos com linha e coluna, onde *element* pode ser um *Button, CheckBox, ComboBox, DatePicker, TimePicker, ListBox, PasswordBox, ProgressBar, RadioButton, StackPanel, StatusBar, TabControl, TextBlock, TabItem, TextBox, ToolBar, TreeView, Groupbox* ou *Label*.

![alt tag](http://s9.postimg.org/xkta58vv3/elementos.gif)

**elementc**
```xml
<Element Grid.Column="0" />
```

**elementr**
```xml
<Element Grid.Row="0" />
```

**elementcr**
```xml
<Element Grid.Column="0" Grid.Row="0" />
```

**elementrc**
```xml
<Element Grid.Row="0" Grid.Column="0" />
```

### Propriedades
------------------
Comandos para adicionar propriedades em um elemento já definido.

![alt tag](http://s29.postimg.org/jrgsasr5z/propriedades.gif)

**col**
```xml
Grid.Column="0"
```

**row**
```xml
Grid.Row="0"
```

**rowcol**
```xml
Grid.Column="0" Grid.Row="0"
```

**colrow**
```xml
Grid.Column="0" Grid.Row="0"
```

**content**
```xml
Content="{x:Static resources:Resource.SMART_COMPLETION}"
```

**cbtemplate**
```xml
<ComboBox.ItemTemplate>
    <DataTemplate>
        <TextBlock Text="{Binding SMART_COMPLETION}" />
    </DataTemplate>
</ComboBox.ItemTemplate>
```

**lbtemplate**
```xml
<ListBox.ItemTemplate>
    <DataTemplate>
        <TextBlock Text="{Binding SMART_COMPLETION}" />
    </DataTemplate>
</ListBox.ItemTemplate>
```

**hasbook**
```xml
Visibility="{Binding SMART_COMPLETION[1].SMART_COMPLETION[2].HasBook,  
                Converter={StaticResource BollToVisibilityConverter}}"
```


### Múltiplos
------------------
Você também pode criar múltiplos de `<Grid.ColumnDefinitions>` e  `<Grid.RowDefinitions>`

![alt tag](http://s17.postimg.org/xdzewvm2n/multiplos.gif)

*Para múltiplas colunas:*

**2cold**
~~~~~xml
<ColumnDefinition Width="Auto" />
<ColumnDefinition Width="Auto" />
~~~~~

**3cold**
~~~~~xml
<ColumnDefinition Width="Auto" />
<ColumnDefinition Width="Auto" />
<ColumnDefinition Width="Auto" />
~~~~~

**4cold**
~~~~~xml
<ColumnDefinition Width="Auto" />
<ColumnDefinition Width="Auto" />
<ColumnDefinition Width="Auto" />
<ColumnDefinition Width="Auto" />
~~~~~

**5cold**
~~~~~xml
<ColumnDefinition Width="Auto" />
<ColumnDefinition Width="Auto" />
<ColumnDefinition Width="Auto" />
<ColumnDefinition Width="Auto" />
<ColumnDefinition Width="Auto" />
~~~~~

*Para múltiplas linhas:*

**2rowd**
~~~~~xml
<RowDefinition Height="Auto" />
<RowDefinition Height="Auto" />
~~~~~

**3rowd**
~~~~~xml
<RowDefinition Height="Auto" />
<RowDefinition Height="Auto" />
<RowDefinition Height="Auto" />
~~~~~

**4rowd**
~~~~~xml
<RowDefinition Height="Auto" />
<RowDefinition Height="Auto" />
<RowDefinition Height="Auto" />
<RowDefinition Height="Auto" />
~~~~~

**5rowd**
~~~~~xml
<RowDefinition Height="Auto" />
<RowDefinition Height="Auto" />
<RowDefinition Height="Auto" />
<RowDefinition Height="Auto" />
<RowDefinition Height="Auto" />
~~~~~

### Changelog
------------------
*Apenas os cinco últimos*

**2.2** - Adicionado "cbtemplate, lbtemplate e hasbook"  
**2.1** - Adicionado "content"  
**2.0** - Adicionado "grid"  
**1.9** - Remoção de "controls"  
**1.8** - Adicionado "element"   
...  
# wpfSnippet
-----------------------------------
Coleção de Snippets e métodos ágeis para melhor produtividade no desenvolvimento em Windows Presentation Foundation, através de Visual Studio + [ReSharper](https://www.jetbrains.com/resharper/download/). Digite o comando, aperte TAB e veja a mágica acontecer. :)

### Getting started
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

**gridcd**
~~~~~xml
<Grid.ColumnDefinitions>
    <ColumnDefinition Width="0" />
</Grid.ColumnDefinitions>
~~~~~

**cold**
~~~~~xml
<ColumnDefinition Width="0" />
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
    <RowDefinition Height="0" />
</Grid.RowDefinitions>
~~~~~

**rowd**
~~~~~xml
<RowDefinition Height="0" />
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
Comandos para adicionar elementos básicos já preenchidos com linha e coluna, onde *element* pode ser um *Button, CheckBox, ComboBox, DatePicker, TimePicker, ListBox, PasswordBox, ProgressBar, RadioButton, StackPanel, StatusBar, TabControl, TextBlock, TabItem, TextBox, ToolBar, TreeView* ou *Label*.

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

### Múltiplos
------------------
Você também pode criar múltiplos de `<Grid.ColumnDefinitions>` e  `<Grid.RowDefinitions>`

![alt tag](http://s17.postimg.org/xdzewvm2n/multiplos.gif)

*Para múltiplas colunas:*

**2cold**
~~~~~xml
<ColumnDefinition Width="0" />
<ColumnDefinition Width="0" />
~~~~~

**3cold**
~~~~~xml
<ColumnDefinition Width="0" />
<ColumnDefinition Width="0" />
<ColumnDefinition Width="0" />
~~~~~

**4cold**
~~~~~xml
<ColumnDefinition Width="0" />
<ColumnDefinition Width="0" />
<ColumnDefinition Width="0" />
<ColumnDefinition Width="0" />
~~~~~

**5cold**
~~~~~xml
<ColumnDefinition Width="0" />
<ColumnDefinition Width="0" />
<ColumnDefinition Width="0" />
<ColumnDefinition Width="0" />
<ColumnDefinition Width="0" />
~~~~~

*Para múltiplas linhas:*

**2rowd**
~~~~~xml
<RowDefinition Height="0" />
<RowDefinition Height="0" />
~~~~~

**3rowd**
~~~~~xml
<RowDefinition Height="0" />
<RowDefinition Height="0" />
<RowDefinition Height="0" />
~~~~~

**4rowd**
~~~~~xml
<RowDefinition Height="0" />
<RowDefinition Height="0" />
<RowDefinition Height="0" />
<RowDefinition Height="0" />
~~~~~

**5rowd**
~~~~~xml
<RowDefinition Height="0" />
<RowDefinition Height="0" />
<RowDefinition Height="0" />
<RowDefinition Height="0" />
<RowDefinition Height="0" />
~~~~~
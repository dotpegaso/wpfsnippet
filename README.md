# wpfSnippet
-----------------------------------
Coleção de Snippets e métodos ágeis para melhor produtividade no desenvolvimento em Windows Presentation Foundation, através de Visual Studio + ReSharper

### Getting started
------------------

- [Baixe](https://github.com/dotpegaso/wpfsnippet/archive/master.zip) o arquivo e entre na pasta *Snippets*
- Abra o `Visual Studio` e em seu menu superior, navegue até `Resharper > Tools > Templates Explorer`
- Em `Scopes` selecione `Global` e clique em `Import` e adicione os snippets ao seu **ReSharper**

![alt tag](http://s18.postimg.org/bf2bzy8op/example.gif)

### Estrutura básica
------------------
- O comando **controls:** é equivalente à uma estrutura básica de nova janela, use-o sempre que criar um novo arquivo .xaml:
~~~~~xml
<controls:BdsElysiumWindow
x:Class="NAMESPACE.View.**[NOME_DA_TELA]**"
xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
xmlns:params="http://schemas.codeplex.com/elysium/params"
xmlns:resources="clr-namespace:Bds.Bdsh.Excel.Vsto.Consult.Resources"
xmlns:controls="clr-namespace:Bds.Bdsh.Excel.Vsto.Consult.Controls"
xmlns:ff="clr-namespace:Bds.Bdsh.Excel.Vsto.Consult.FunctionalFun.UI"
xmlns:extra="http://schemas.extra.com/ui"
xmlns:metro="http://schemas.codeplex.com/elysium"
xmlns:viewModel="clr-namespace:Bds.Bdsh.Excel.Vsto.Consult.ViewModel"
xmlns:utils="clr-namespace:Bds.Bdsh.Excel.Vsto.Consult.Utils"
xmlns:i="http://schemas.microsoft.com/expression/2010/interactivity"
mc:Ignorable="d"
d:DesignHeight="600" d:DesignWidth="800"
Height="600" Width="800"
TitleBarBackground="#FF1F6F43"
params:Design.AccentBrush="#FF1F6F43"
TitleBarForeground="White"
WindowStartupLocation="CenterOwner"
WindowState="Normal"
DataContext="{Binding RelativeSource={RelativeSource Self}, Path=ViewModel, Mode=TwoWay, UpdateSourceTrigger=PropertyChanged}"
Title="{x:Static resources:Resource.**[NOME_DA_TELA]**_TitleBar}">
<!--VOCÊ PODE ALTERAR O TAMANHO DA TELA ACIMA, NA PROPRIEDADE "Height="" Width=""-->
<!--NÃO ESQUEÇA DE INSERIR O NOME DA SUA TELA NAS PROPRIEDADES x:Class="" & Title=""-->

<Grid Margin="5">
    <!--INICIE O CÓDIGO AQUI-->
</Grid>

</controls:BdsElysiumWindow>
~~~~~

### Estrutura de Grids
------------------
Os comandos abaixo faciltam a construção de markdown para criação de grids e suas propriedades.
Para decorar os comandos, lembre-se das iniciais maiúsculas que vão após o início da marcação.

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
Comandos para adicionar elementos básicos já preenchidos com linha e coluna

Exemplo: `elementr+TAB` se transforma em
```xml
<Button Grid.Row="0" />
```

**elementc**
```xml
<Button Grid.Column="0" />
```

**elementr**
```xml
<Button Grid.Row="0" />
```

**elementcr**
```xml
<Button Grid.Column="0" Grid.Row="0" />
```

**elementrc**
```xml
<Button Grid.Row="0" Grid.Column="0" />
```

### Propriedades
------------------
Comandos para adicionar propriedades em uma marcação.

Exemplo: `<Label row+TAB />` se transforma em:
```xml
<Label Grid.Row="0"/>
```

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
Você também pode criar múltiplos `<Grid.ColumnDefinitions>` e  `<Grid.RowDefinitions>`

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
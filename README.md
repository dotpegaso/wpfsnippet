# wpfSnippet

Coleção de Snippets e métodos ágeis para melhor produtividade no desenvolvimento em Windows Presentation Foundation, através de Visual Studio + ReSharper

### Getting started

- [Baixe](https://github.com/dotpegaso/wpfsnippet/archive/master.zip) o arquivo e entre na pasta Snippets
- Abra o `Visual Studio` e em seu menu superior, navegue até `Resharper > Tools > Templates Explorer`
- Em `Scopes` selecione `Global` e clique em `Import`

![alt tag](http://s18.postimg.org/bf2bzy8op/example.gif)

### Estrutura básica

- O comando **controls:** é equivalente à uma estrutura básica de nova janela, o sempre que criar um novo arquivo .xaml:
```
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
```

### Estrutura de Grids
Os comandos abaixo faciltam a construção de markdown para criação de grids e suas propriedades.
Para decorar os comandos, lembre-se das iniciais maiúsculas que vão após o início da marcação.
Exemplo: `<**Grid**.**R**ow**D**efinitions>` => `grid**rd**`


- **gridcd** =
```
<Grid.ColumnDefinitions>
    <ColumnDefinition Width="0" />
</Grid.ColumnDefinitions>
```

- **cold** =
```
<ColumnDefinition Width="0" />
```

- **gridc** =
```
<Grid Grid.Column="0" Margin="5">
</Grid>
```

- **gridrd** =
```
<Grid.RowDefinitions>
    <RowDefinition Height="0" />
</Grid.RowDefinitions>
```

- **rowd** =
```
<RowDefinition Height="0" />
```

- **gridr** =
```
<Grid Grid.Row="0" Margin="5">
</Grid>
```

- **gridrc** =
```
<Grid Grid.Row="0" Grid.Column="0" Margin="5">
</Grid>
```

- **gridcr** =
```
<Grid Grid.Column="0" Grid.Row="0" Margin="5">
</Grid>
```

### Propriedades estes comandos para adicionar propriedades em um componente

  - **col** =
        `Grid.Column="0"`

Exemplo
    
    `<Label />` > `<Label col+**TAB** /> **=>** `<Label Grid.Column="0"/>` 


  - **row** =
        `Grid.Row="0"`

Exemplo
    
    `<Label />` > `<Label row+**TAB** /> **=>** `<Label Grid.Row="0"/>`


  - **rowcol** =
        `Grid.Column="0"`

Exemplo
    
    `<Label />` > `<Label rowcol+**TAB** /> **=>** `<Label Grid.Row="0" Grid.Column="0"/>`


  - **colrow** =
        `Grid.Column="0"`

Exemplo
    
    `<Label />` > `<Label colrow+**TAB** /> **=>** `<Label Grid.Column="0" Grid.Row="0"/>`


### Múltiplos

Você também pode criar múltiplos `<Grid.ColumnDefinitions>` e  `<Grid.RowDefinitions>`

Para múltiplas colunas:

- **2cold** para:
  ```
<ColumnDefinition Width="0" />
<ColumnDefinition Width="0" />
  ```

  - **3cold** para:
        <ColumnDefinition Width="0" />
        <ColumnDefinition Width="0" />
        <ColumnDefinition Width="0" />

  - **4cold** para:
        <ColumnDefinition Width="0" />
        <ColumnDefinition Width="0" />
        <ColumnDefinition Width="0" />
        <ColumnDefinition Width="0" />

  - **5cold** para:
        <ColumnDefinition Width="0" />
        <ColumnDefinition Width="0" />
        <ColumnDefinition Width="0" />
        <ColumnDefinition Width="0" />
        <ColumnDefinition Width="0" />

Para múltiplas linhas:

  - **2rowd** para:
        <RowDefinition Height="0" />
        <RowDefinition Height="0" />

  - **3rowd** para:
        <RowDefinition Height="0" />
        <RowDefinition Height="0" />
        <RowDefinition Height="0" />

  - **4rowd** para:
        <RowDefinition Height="0" />
        <RowDefinition Height="0" />
        <RowDefinition Height="0" />
        <RowDefinition Height="0" />

  - **5rowd** para:
        <RowDefinition Height="0" />
        <RowDefinition Height="0" />
        <RowDefinition Height="0" />
        <RowDefinition Height="0" />
        <RowDefinition Height="0" />
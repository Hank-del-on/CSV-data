ASP.NET Core-prosjekt

 .NET Framework 4.5 but my new library is running .NET Framework 4.5.2

dotnet run

@model IEnumerable<CsvReaderApp.Models.camera>

@{
    ViewData["Title"] = "Camera Datasett";
}

<h1>camera Datasett</h1>

<form asp-action="Search" method="post">
    <input type="number" name="id" placeholder="Skriv inn ID" required />
    <button type="submit">Søk</button>
</form>

@if (Model != null && Model.Any())
{
    <table>
        <thead>
            <tr>
                <th>ID</th>
                <th>Navn</th>
                <th>Alder</th>
            </tr>
        </thead>
        <tbody>
            @foreach (var camera in Model)
            {
                <tr>
                    <td>@camera.Id</td>
                    <td>@camera.Navn</td>
                    <td>@camera.Alder</td>
                </tr>
            }
        </tbody>
    </table>
}
else
{
    <p>Ingen camera funnet med den IDen.</p>
}
--


[missing css]

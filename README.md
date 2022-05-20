# Ordenar-3-numeros-con-GoTo-en-Visual-Basic1
Mediante uso de GOTO en visual Basic, realice el ordenamiento de 3 números.------1er parcial 319

Public Class Form1
    Private Sub Button1_Click(sender As Object, e As EventArgs) Handles Button1.Click
        Dim a, b, c, z As Integer
        Dim aux As String
        a = Convert.ToInt32(TextBox1.Text)
        b = Convert.ToInt32(TextBox2.Text)
        c = Convert.ToInt32(TextBox3.Text)
        If a > b Then
            z = a
            a = b
            b = z
        End If
        If b > c Then
            z = b
            b = c
            c = z
        End If
        If b < a Then
            z = a
            a = b
            b = z
            GoTo final
        Else
            GoTo final
        End If
final:
        aux = a & ", " & b & ", " & c
        TextBox4.Text = aux
        GoTo salir
salir:
    End Sub

    Private Sub Button2_Click(sender As Object, e As EventArgs) Handles Button2.Click
        Dim a, b, c, z As Integer
        Dim aux As String
        a = Convert.ToInt32(TextBox1.Text)
        b = Convert.ToInt32(TextBox2.Text)
        c = Convert.ToInt32(TextBox3.Text)
        If a < b Then
            z = a
            a = b
            b = z
        End If
        If b < c Then
            z = b
            b = c
            c = z
        End If
        If b > a Then
            z = a
            a = b
            b = z
            GoTo final
        Else
            GoTo final
        End If
final:
        aux = a & ", " & b & ", " & c
        TextBox4.Text = aux
        GoTo salir
salir:
    End Sub
End Class

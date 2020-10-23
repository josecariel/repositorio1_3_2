# repositorio1_3_2
/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package com.cariel.sistemas.ventanaboton;
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;
import java.util.Date;
/**
 *
 * @author jose cariel reyes bautista
 */
public class VentanaBotonEscuchador extends JFrame implements ActionListener{
     JPanel panelBoton;
    JLabel etiqueta;
    JButton boton; 
    
    public VentanaBotonEscuchador(){
etiqueta = new JLabel();
panelBoton = new JPanel();
boton = new JButton("Pulsa aqui");
panelBoton.add(boton);
this.getContentPane().setLayout(new BorderLayout());
this.getContentPane().add(etiqueta, "North");
this.getContentPane().add(panelBoton, "South");
boton.addActionListener(this);
this.setSize(300, 100);
this.setTitle("ejemplo de un boton con evento 2");
this.show();
}
   @Override 
   public void actionPerformed(ActionEvent e){
   etiqueta.setText("Boton pulsado: " + new Date());
   }
   public static void main (String[] args){
       new VentanaBotonEscuchador();
   }
   
}

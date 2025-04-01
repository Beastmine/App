import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  template: `
    <ion-app>
      <ion-menu contentId="main-content">
        <ion-header>
          <ion-toolbar>
            <ion-title>CropGuru</ion-title>
          </ion-toolbar>
        </ion-header>
        <ion-content>
          <ion-list>
            <ion-item button (click)="navigate('home')">Home</ion-item>
            <ion-item button (click)="navigate('categories')">Categories</ion-item>
          </ion-list>
        </ion-content>
      </ion-menu>

      <div id="main-content">
        <ion-header>
          <ion-toolbar>
            <ion-buttons slot="start">
              <ion-menu-button></ion-menu-button>
            </ion-buttons>
            <ion-title>CropGuru</ion-title>
          </ion-toolbar>
        </ion-header>

        <ion-content>
          <ion-searchbar placeholder="Search for crops..."></ion-searchbar>

          <div class="delivery-box">
            Deliver to Yashmine
          </div>

          <div class="new-section">
            <h2>NEW</h2>
            <p>Newly arrived crops will be displayed here.</p>
          </div>

          <div class="offer-box">
            Flat Rs.100 on first choose
          </div>

          <div class="categories-section">
            <h2>Crops</h2>
            <ion-grid>
              <ion-row>
                <ion-col><ion-button expand="full">Fruits</ion-button></ion-col>
                <ion-col><ion-button expand="full">Vegetables</ion-button></ion-col>
              </ion-row>
              <ion-row>
                <ion-col><ion-button expand="full">Grains</ion-button></ion-col>
                <ion-col><ion-button expand="full">Atta</ion-button></ion-col>
              </ion-row>
              <ion-row>
                <ion-col><ion-button expand="full">Rice</ion-button></ion-col>
              </ion-row>
            </ion-grid>
          </div>
        </ion-content>
      </div>
    </ion-app>
  `,
  styles: [
    `
      .delivery-box, .offer-box {
        padding: 10px;
        background-color: #f8f8f8;
        text-align: center;
        margin: 10px;
        border-radius: 5px;
      }
      .new-section, .categories-section {
        padding: 15px;
      }
      .categories-section ion-button {
        width: 100%;
      }
    `
  ]
})
export class AppComponent {
  navigate(route: string) {
    console.log(`Navigating to ${route}`);
  }
}

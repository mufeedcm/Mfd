import math

def frequency_to_time():
    f = float(input("\nEnter Frequency (Hz): "))
    if f > 0:
        T = 1 / f
        print(f"Time Period (T) = {T} seconds")
    else:
        print("Frequency must be greater than zero.")

def time_to_frequency():
    T = float(input("\nEnter Time Period (seconds): "))
    if T > 0:
        f = 1 / T
        print(f"Frequency (f) = {f} Hz")
    else:
        print("Time period must be greater than zero.")

def wavelength_calculation():
    v = float(input("\nEnter Wave Speed (m/s), e.g., 3.0e8 for light: "))
    f = float(input("Enter Frequency (Hz): "))
    if f > 0:
        wavelength = v / f
        print(f"Wavelength (λ) = {wavelength} meters")
    else:
        print("Frequency must be greater than zero.")

def angular_frequency():
    f = float(input("\nEnter Frequency (Hz): "))
    if f > 0:
        omega = 2 * math.pi * f
        print(f"Angular Frequency (ω) = {omega} rad/s")
    else:
        print("Frequency must be greater than zero.")

def damped_frequency():
    f0 = float(input("\nEnter Natural Frequency (Hz): "))
    zeta = float(input("Enter Damping Ratio (ζ): "))

    if f0 > 0 and 0 <= zeta < 1:
        fd = f0 * math.sqrt(1 - zeta**2)
        print(f"Damped Frequency (fd) = {fd} Hz")
    else:
        print("Ensure f0 > 0 and 0 ≤ ζ < 1.")

def main():
    while True:
        print("\nElectronics Frequency & Time Calculator")
        print("1. Frequency to Time Period")
        print("2. Time Period to Frequency")
        print("3. Wavelength Calculation")
        print("4. Angular Frequency")
        print("5. Damped Frequency (RLC Circuit)")
        print("6. Exit")

        choice = input("Choose an option (1-6): ")

        if choice == '1':
            frequency_to_time()
        elif choice == '2':
            time_to_frequency()
        elif choice == '3':
            wavelength_calculation()
        elif choice == '4':
            angular_frequency()
        elif choice == '5':
            damped_frequency()
        elif choice == '6':
            print("Exiting... Goodbye!")
            break
        else:
            print("Invalid choice. Try again.")

if __name__ == "__main__":
    main()
using UnityEngine;

public class CameraMovement : MonoBehaviour
{
    public float movementSpeed = 5f;

    void Update()
    {
        float verticalInput = Input.GetAxis("Vertical");

        Vector3 movement = new Vector3(0f, verticalInput, 0f) * movementSpeed * Time.deltaTime;
        transform.position += movement;
    }
}
